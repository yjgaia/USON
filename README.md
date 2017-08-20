# USON
USON :: Universal types included JSON.

* boolean
* number
* string
* array
* ***Date***
* ***function***
* ***prototype***

USON는 [UPPERCASE-CORE](https://github.com/Hanul/UPPERCASE/blob/master/DOC/GUIDE/UPPERCASE-CORE.md)를 기반으로 만들어졌습니다.

## 사용 방법
### Node.js 환경
```
npm install -s uson.js
```
```javascript
require('uson.js');
```

### 웹 브라우저 환경
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
	
	let Person = function(firstName, lastName) {
		this.firstName = firstName;
		this.lastName = lastName;
	};
	
	Person.prototype.getName = function() {
		return this.firstName + ' ' + this.lastName;
	};

	let originData = {
		Person : Person,
		person : new Person('Young Jae', 'Sim')
	};
	
	let newData = USON.parse(USON.stringify(originData));
	
	console.log(new newData.Person('Young Jae', 'Sim').getName());
	console.log(newData.person.getName());
});
</script>
```

## 라이센스
[MIT](LICENSE)

## 작성자
[Young Jae Sim](https://github.com/Hanul)
