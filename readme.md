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
            @cf_label_align:            left;
            @cf_form_width:             512px;
            @cf_form_left_width:        256px;
            @cf_form_right_width:       256px;
            @cf_gutter_width:           16px;
            @cf_element_margin_bottom:  16px;
            @cf_element_border_color:   #bfbfbf;
            @cf_element_border_size:    1px;
            @cf_element_height:         24px;
            @cf_textarea_height:        192px;
            @cf_select_multiple_height: 96px;

            @cf_error_background_color: #ffefef;
            @cf_error_color:            #bf0000;
            @cf_error_margin_top:       -8px;
            @cf_error_margin_bottom:    8px;

            @cf_help_color:             #7f7f7f;
            @cf_help_margin_top:        -8px;
            @cf_help_margin_bottom:     8px;

            .clean_form;
            .clean_form_error;
            .clean_form_help;
        }

        form.baz {
            @cf_label_align:            right;

            .clean_form;
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
