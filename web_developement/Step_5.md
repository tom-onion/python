Nice! Now that your project is running and `makemigrations` is working, you're ready for:

---

## 🪜 **Step 5: Build Models and Connect to a Database**

This step lets you define the **structure of your data** (like blog posts, users, comments) using Django’s ORM (Object Relational Mapper).

---

### ✅ 1. **Create a Model**

In your app’s `models.py` (e.g., `blog/models.py`):

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
    created_at = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

---

### ✅ 2. **Create & Apply Migrations**

```bash
python manage.py makemigrations
python manage.py migrate
```

Django will now create a `Post` table in your SQLite database (default DB).

---

### ✅ 3. **Register the Model in Admin Panel**

In `blog/admin.py`:

```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

---

### ✅ 4. **Create a Superuser (If You Haven't)**

```bash
python manage.py createsuperuser
```

It’ll ask you for username, email, password. After that:

```bash
python manage.py runserver
```

Visit: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)  
Log in with your superuser credentials.

🎉 You can now **create and manage Posts** in the admin panel!

---

### 🧪 Optional Test

Try adding a few blog posts through the admin panel and confirm they show up in the database.

---

### 🟦 Up Next (Step 6):  
Let’s **display those posts on your site using templates**. We'll create a proper homepage that pulls blog data from the database and shows it in HTML.

Want to continue with that?