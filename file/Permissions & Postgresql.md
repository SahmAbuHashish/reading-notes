# Reading Questions

### What are the key components and purpose of Django Rest Framework (DRF) permissions, and how do they help in securing an API?

Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.

Permissions are used to grant or deny access for different classes of users to different parts of the API.

The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the IsAuthenticated class in REST framework.

A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the IsAuthenticatedOrReadOnly class in REST framework.

1. Permissions classes.
2. Purpose of permissions.
3. Default permissions.
4. Custom permissions.
5. Permission checks.
6. Permission decorators.

---

### In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?

In SQL, the SELECT statement is used to retrieve data from a database table. It allows you to specify which columns you want to retrieve and apply filtering or sorting conditions if needed. The SELECT statement is a fundamental component of SQL queries and provides the ability to extract specific data from one or more tables.

- To retrieve all columns from a table called 'employees' using the SELECT statement, you would use the following query:

```sql
SELECT * FROM employees;
```

---

### Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?

DRF (Django REST Framework) Generic Views are pre-built view classes provided by DRF that simplify the implementation of common API patterns. They are designed to handle common CRUD (Create, Retrieve, Update, Delete) operations in a concise and reusable manner. The role of DRF Generic Views is to abstract away repetitive code and provide a standard way to define API views.

Typically when using the generic views, you'll override the view, and set several class attributes.

```python
from django.contrib.auth.models import User
from myapp.serializers import UserSerializer
from rest_framework import generics
from rest_framework.permissions import IsAdminUser

class UserList(generics.ListCreateAPIView):
    queryset = User.objects.all()
    serializer_class = UserSerializer
    permission_classes = [IsAdminUser]
```    

For more complex cases you might also want to override various methods on the view class. For example.

```python
class UserList(generics.ListCreateAPIView):
    queryset = User.objects.all()
    serializer_class = UserSerializer
    permission_classes = [IsAdminUser]

    def list(self, request):
        # Note the use of `get_queryset()` instead of `self.queryset`
        queryset = self.get_queryset()
        serializer = UserSerializer(queryset, many=True)
        return Response(serializer.data)
```  

For very simple cases you might want to pass through any class attributes using the .as_view() method. For example, your URLconf might include something like the following entry:

```python
path('users/', ListCreateAPIView.as_view(queryset=User.objects.all(), serializer_class=UserSerializer), name='user-list')
```  
