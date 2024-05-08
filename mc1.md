# Mini Challenge 1

## Message board

## pre-req
Your base template must, at a minimum, have the links corresponding to bootstrap integration as demonstrated in previous classes and a navbar of your choosing (navbars must be bootstrap compatible).

### Acceptance Criteria
1. Your `list.html` template should, at a minimum, allow users to click a link to access any rendered post and that link should go to that post's detail page.
2. Your navbar should contain a link that takes users to the new post form.
3. When you submit the new post form you will get an error (stack trace).
3.1. To solve the error, implement the `get_absolute_url` method on your `Post` model (see snippet below).
3.2. When your form is successfully submitted, it should take users to that new post's `detail` page.


## Example
```
from django.urls import reverse

...
    def get_absolute_url(self):
        return reverse("detail", args=[self.id])
```

### Bonus
See if you can, as an experiment, make it so that users are redirected to the list of posts instead of the post's detail page.