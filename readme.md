# clean_form

A customizable, extendable, and maintainable HTML form styled using
[less.js](https://github.com/cloudhead/less.js/). The form is designed to have
a consistent look among the fields, and the elements that receive input should
look native on all platforms.

# Set up

1. Copy `clean_form.less` to your CSS directory.

2. Modify `clean_form.less` by creating one or more form classes. There is
   already a `clean_form_test` class that you can modify.

3. `lessc clean_form.less clean_form.css`.

4. Modify the structure of your HTML forms so that they match the one in
   `clean_form_test.html`.

5. Add `<link rel="stylesheet" href="clean_form.css">` to `head` of your
   HTML file.

6. You probably also want to set the typography for all the form elements.

        body, input, select, textarea {
            font: 16px/1.5 sans-serif;
        }

7. Refresh.

## License

Copyright © 2010–2011, Alexander Teinum <ateinum@gmail.com>

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED “AS IS” AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF
THIS SOFTWARE.
