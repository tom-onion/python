Yesss, let’s do it! 🔐  
**Step 9: Add User Authentication (Login, Logout, and Register)** — this gives your site **user accounts**, so only registered users can create or manage posts.

---

## 🧑‍💻 **Step 9: User Authentication in Django**

Django comes with a **built-in authentication system**, which makes this step pretty smooth.

---

### ✅ 1. **Enable Django’s Auth System**

Make sure `'django.contrib.auth'` and `'django.contrib.sessions'` are in your `INSTALLED_APPS` (they usually are by default in `settings.py`).

Also check middleware:

```python
MIDDLEWARE = [
    ...
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
]
```

---

### ✅ 2. **Create Login & Logout Views**

You don’t even need to write them — Django provides them! Just connect them in `urls.py`.

In `mysite/urls.py`:

```python
from django.contrib.auth import views as auth_views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('blog.urls')),
    path('login/', auth_views.LoginView.as_view(template_name='blog/login.html'), name='login'),
    path('logout/', auth_views.LogoutView.as_view(next_page='home'), name='logout'),
]
```

---

### ✅ 3. **Create Login Template**

Create `login.html` inside `blog/templates/blog/`:

```html
<h2>Login</h2>
<form method="POST">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Login</button>
</form>
```

And somewhere in your base/home page, add:

```html
{% if user.is_authenticated %}
    <p>Welcome, {{ user.username }}! <a href="{% url 'logout' %}">Logout</a></p>
{% else %}
    <a href="{% url 'login' %}">Login</a>
{% endif %}
```

---

### ✅ 4. **Protect the “Add Post” Page**

Only allow logged-in users to add a post:

In `blog/views.py`, add the decorator:

```python
from django.contrib.auth.decorators import login_required

@login_required
def add_post(request):
    ...
```

If a user tries to access `/add/` without being logged in, they’ll be redirected to `/login/`.

---

### ✅ 5. **Add Registration (Sign Up)**

Django doesn’t give you a built-in view for this — but we can create one easily!

**In `blog/forms.py`:**

```python
from django.contrib.auth.forms import UserCreationForm
from django.contrib.auth.models import User

class RegisterForm(UserCreationForm):
    class Meta:
        model = User
        fields = ['username', 'password1', 'password2']
```

**In `views.py`:**

```python
from .forms import RegisterForm

def register(request):
    if request.method == 'POST':
        form = RegisterForm(request.POST)
        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = RegisterForm()
    return render(request, 'blog/register.html', {'form': form})
```

**In `blog/urls.py`:**

```python
path('register/', views.register, name='register'),
```

**Create `register.html`:**

```html
<h2>Register</h2>
<form method="POST">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Register</button>
</form>
```

---

### ✅ 6. **Try It Out**

- Go to `/register/` → create an account
- Then log in at `/login/`
- Now you can access `/add/` 🎉

---

### 🎁 Bonus (for the future):

- Use Django messages to show success alerts
- Style forms with Tailwind or Bootstrap
- Add email verification

---
