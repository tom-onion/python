Let’s gooo 🚀  
You’ve got a homepage showing posts — now it’s time to build **individual blog post pages**!

---

## 📄 **Step 7: Create Post Detail View (Dynamic Pages)**

Each blog post should have its **own unique URL** (like `/post/3/`), and a page to show full content.

---

### ✅ 1. **Update Your App URLs for Detail View**

In `blog/urls.py`, add this route:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home, name='home'),
    path('post/<int:post_id>/', views.post_detail, name='post_detail'),  # ← this!
]
```

---

### ✅ 2. **Create the Detail View**

In `blog/views.py`, add:

```python
from django.shortcuts import get_object_or_404

def post_detail(request, post_id):
    post = get_object_or_404(Post, id=post_id)
    return render(request, 'blog/post_detail.html', {'post': post})
```

---

### ✅ 3. **Create the Detail Template**

Make a new file `post_detail.html` in `blog/templates/blog/`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>{{ post.title }}</title>
</head>
<body>
    <a href="/">← Back to Home</a>
    <h1>{{ post.title }}</h1>
    <p>{{ post.content }}</p>
    <small>Posted on {{ post.created_at }}</small>
</body>
</html>
```

---

### ✅ 4. **Link Posts from Homepage to Detail View**

Update your `home.html` like this:

```html
<h1>Blog Posts</h1>
{% for post in posts %}
    <div style="margin-bottom: 20px;">
        <h2><a href="{% url 'post_detail' post.id %}">{{ post.title }}</a></h2>
        <p>{{ post.content|truncatechars:100 }}</p>
        <small>Posted on {{ post.created_at }}</small>
    </div>
{% empty %}
    <p>No posts yet!</p>
{% endfor %}
```

---

### ✅ 5. **Test It!**

Run the server:

```bash
python manage.py runserver
```

- Go to [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- Click on a post title — it should take you to `/post/1/` or whatever ID and show full content.

---

### 🎁 Bonus Ideas:
- Add slugs for cleaner URLs (e.g., `/post/my-first-post/`)
- Use Bootstrap for layout
- Add comments (coming soon)

---

Wanna go for **Step 8: Add forms and let users create posts via the site**? Or build something else on top of this?