# USON
USON :: Universal types included JSON.

- boolean
- number
- string
- array
- Date
- function

##### Usage
    <script>
        global = window;
    </script>
    <script src="UPPERCASE.JS"></script>
    <script src="USON.js"></script>
    <script>
        global.onload = function() {

            // init all singleton classes.
            OBJECT.init();

            var
            // data
            data = {
                msg : 'test',
                date : new Date(),
                func : function() {
                    console.log('ok!');
                }
            };

            // where are date and func?
            console.log(JSON.parse(JSON.stringify(data)));

            // work correct.
            console.log(USON.parse(USON.stringify(data)));

            // ok!
            USON.parse(USON.stringify(data)).func();
        };
    </script>

##### License
https://bitbucket.org/uppercaseio/uppercase.js/src/007c711583d32a9fcea26fd0ea5c3bf9b76dd2a6/LICENSE.md


2014 ⓒ BTNcafe · http://www.btncafe.com · contact@btncafe.com
