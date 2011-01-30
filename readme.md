# clean_form

Style HTML forms with less.js.

## Setup

1. Copy `clean_form.less` to your website directory.

2. Define as many form configurations as you need in a separate `less`-file.

       @import url('clean_form.less');

       form#foo {
           .clean_form;
       }

       form.bar {
           .clean_form(
               left,    // label_align
               512px,   // form_width
               256px,   // form_left_width
               256px,   // form_right_width
               16px,    // gutter_width
               24px,    // field_height
               16px,    // field_margin_bottom
               #bfbfbf, // element_border_color
               1px,     // element_border_size
               192px,   // textarea_height
               128px);  // select_multiple_height
       }

       form.baz {
           .clean_form(right);
       }

3. Compile. E.g. `lessc test.less test.css`.

4. Use the HTML structure defined in `test.html`. This is an example.

       <form id="foo">
           <div>
               <label for="input_text">Label for text input</label>
               <input id="input_text" type="text">
               <div style="clear: both;"></div>
           </div>
       </form>

5. You probably also want to set the typography for all the form elements.

       body, input, select, textarea {
           font: 16px/1.5 sans-serif;
       }

## Additional features

### Error text

    form {
        .clean_form;
        .clean_form_error(
            #ffefef, // error_background_color
            #bf0000, // error_color
            8px,     // error_margin_top
            8px);    // error_margin_bottom
    }

### Help text

    form {
        .clean_form;
        .clean_form_help(
            #7f7f7f, // help_color
            8px,     // help_margin_top
            8px);    // help_margin_bottom
    }

### Date

    form {
        .clean_form;
        .clean_form_date(
            256px, // form_right_width
            16px,  // gutter_width
            48px,  // date_day_width
            64px,  // date_year_width
            8px);  // date_element_margin
    }

## To do

* I would like to add support for horizontal forms. I am not sure what the
  optimal way to structure the code is. The HTML probably doesn’t need the divs.
  For the less.js-part, one option is to create a separate mixin. Another option
  is to integrate it with the existing.

* The labels and input elements are now vertically centered relative to their
  line heights. Aligning text on a baseline is nicer visually, but it might add
  complexity to the CSS. When I find time to do it, I might steal some ideas
  from [Baseline](http://baselinecss.com/).

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
