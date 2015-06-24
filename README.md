*이 프로젝트는 EXTREME.JS(https://github.com/Hanul/EXTREME.JS)에 통합되었습니다.*

# USON
USON :: Universal types included JSON.

- boolean
- number
- string
- array
- Date
- function

USON using UPPERCASE.JS (https://bitbucket.org/uppercaseio/uppercase.js)

##### Usage
    <script>
        global = window;
    </script>
    <!--[if lt IE 9]>
    <script src="JSON.js"></script>
    <![endif]-->
    <script src="UPPERCASE.JS"></script>
    <script src="USON.js"></script>
    <script>
        // if not exists console.log.
        if (global.console === undefined || console.log === undefined || console.log.apply === undefined) {
            global.console = {
                log : function(msg) {
                    alert(msg);
                }
            };
        }

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

##### Updates
- (2014. 4. 27) IE8 support.

##### License
https://bitbucket.org/uppercaseio/uppercase.js/src/007c711583d32a9fcea26fd0ea5c3bf9b76dd2a6/LICENSE.md


2014 ⓒ BTNcafe · http://www.btncafe.com · contact@btncafe.com
