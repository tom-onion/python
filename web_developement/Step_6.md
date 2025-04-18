Let’s roll into **Step 6** – time to make your site come alive! 🌟  
You’ve got data (your `Post` model), now let’s **show it on your website** using Django views + templates.

---

## 🖼️ **Step 6: Display Data Using Templates**

---

### ✅ 1. **Create a View to Fetch Posts**

In `blog/views.py`:

```python
from django.shortcuts import render
from .models import Post

def home(request):
    posts = Post.objects.all().order_by('-created_at')  # newest first
    return render(request, 'blog/home.html', {'posts': posts})
```

---

### ✅ 2. **Create a Template Folder**

Inside your `blog` app folder, create a folder named `templates`, and inside it another folder named `blog`.  
Your structure should look like this:

```
blog/
├── templates/
│   └── blog/
│       └── home.html
```

Now create `home.html` with this basic HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Blog</title>
</head>
<body>
    <h1>Blog Posts</h1>
    {% for post in posts %}
        <div style="margin-bottom: 20px;">
            <h2>{{ post.title }}</h2>
            <p>{{ post.content }}</p>
            <small>Posted on {{ post.created_at }}</small>
        </div>
    {% empty %}
        <p>No posts yet!</p>
    {% endfor %}
</body>
</html>
```

---

### ✅ 3. **Connect the View to a URL**

In `blog/urls.py`, make sure you’ve added:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home, name='home'),
]
```

And in your `mysite/urls.py`, make sure this is included:

```python
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('blog.urls')),  # Connect to blog app
]
```

---

### ✅ 4. **Run the Server and Test**

```bash
python manage.py runserver
```

Now visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

🎉 You should see a list of your blog posts rendered in the browser!

---

### 🧪 Optional Enhancements:
- Add CSS styles
- Show only 5 recent posts
- Link to detail view (Step 7!)
- Use a base layout with `{% block content %}`

---

### ✅ Up Next (Step 7):  
Let’s create a **detailed post page**, so when you click on a blog title, it opens its full content on a separate page.

Wanna move on to that?