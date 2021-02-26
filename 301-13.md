# Forms

## SENDING FORM DATA
Form attributes:
1. `action = "url` : the data will be sent to the specified url / if none to the same page.
2. `method = "GET"` : the data will be sent as a request in the header. (url/?key=value&key2=value2).
3. `method = "POST"` : the data will be sent as a request in the body. (more secure, better for lonfer data, and sending files).

---
## Forms
### Form tag attributes:
- `action = "/path-to-url"`
- `method = "GET/POST"`
- `name = "formName"`
- `autocomplete = "on/off"`
- `target = "_blank" (new tab) / "_self" (current tab)`
- `enctype = "text/plain" (text input form) "multipart/form-data" (forms containing files)`


### Reference
[HTML forms reference](https://htmlreference.io/forms/)