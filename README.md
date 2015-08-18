# postmark-tornado
Tornado Mixin for Postmark


##Usage

```
import tornado.web
import tornado.options
from mixins.postmark_mixin import PostmarkMixin

tornado.options.define('postmark_signature', 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx')
tornado.options.define('postmark_sendemail', 'email@email.com')

class EmailHandler(tornado.web.RequestHandler, PostmarkMixin):
    def post(self):
        to = 'test@test.com'
        body = 'This is test message'
        subject = 'Test Message'
        self.send_email(body=body, to=to, subject=subject)
```
