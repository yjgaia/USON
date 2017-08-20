# USON
USON :: Universal types included JSON.

- boolean
- number
- string
- array
- Date
- function

USON는 [UPPERCASE-CORE](https://github.com/Hanul/UPPERCASE/blob/master/DOC/GUIDE/UPPERCASE-CORE.md)를 기반으로 만들어졌습니다.

## 사용 방법
```html
<script src="UPPERCASE-CORE/BROWSER.js"></script>
<script src="USON.js"></script>
<script>
'use strict';
RUN(() => {
	INIT_OBJECTS();

	let data = {
		msg : 'test',
		date : new Date(),
		func : () => {
			console.log('ok!');
		}
	};

	// where are date and func?
	console.log(JSON.parse(JSON.stringify(data)));

	// work correct.
	console.log(USON.parse(USON.stringify(data)));

	// ok!
	USON.parse(USON.stringify(data)).func();
});
</script>
```

## 라이센스
[MIT](LICENSE)

## 작성자
[Young Jae Sim](https://github.com/Hanul)
