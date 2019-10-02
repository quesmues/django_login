# django_login
Sistema de login/logout usando Django 2.2

Sistema baseado no tutorial do blog: [WSVicent Django Tutorial Login And Logout](https://wsvincent.com/django-user-authentication-tutorial-login-and-logout/)

Foi realizada algumas modificações para que quando o usuário não estiver autenticado ele sempre vai redirecionar para a tela de login, para isso foi utilizado decorator @login_required

O mapeamento das url's foi alterado para não ficar respondendo para todas as urls do app django.contrib.auth, foi utilizada apenas as views de login/logout.

```python
urlpatterns = [
    ...
    path('login/', auth_views.LoginView.as_view(redirect_authenticated_user=True), name='login'),
    path('logout/', auth_views.LogoutView.as_view(), name='logout'),
    ...
]
```
#hacktoberfest
