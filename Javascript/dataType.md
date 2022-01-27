>**`(드림코딩)자바스크립트 기초 강의`를 수강한 후 정리하였습니다.**

</br>

# Data Type
### 📌 let(mutable) vs var / rw(read/write)
    
  <br>

  ```jsx
    // let (added in ES6)
    
    let globalName = "global name";
    
    {
    let name = 'ellie';
    console.log(name);
    
    name = 'hello';
    console.log(name);
    console.log(globalName);
    }
    
    console.log(name);
    console.log(globalName);
    
    // var (don't ever use this!)
    // var hoisting (move declaration from bottom to top)
    // has no block scope
    
    {
        age = 4;
        var age;
    }
    console.log(age);
  ```
    
### 📌 constant(immutable) /  r(read only)
    
  <br>

  ```jsx
    // use const whenever possible
    // only use let if variable needs to change
    // favor immutable data type always for a few reasons;
    // - security
    // - thread safety
    // - reduce human mistakes
    const daysInWeed = 7;
    const maxNumber = 5;
    
    // Note!
    // Immutable data types: primitive types, frozen obejcts (i.e. object.freeze())
    // Mutable data types: all obejcts by default are mutable in JS
    // favor immutabele data type always for a few reasons;
    // - security
    // - thread safety
    // - reduce human mistakes
  ```
  
  <br/>

### 📌 Variable types

  <br/>
    
  ```jsx
    // primitive, single item: number, string, boolean, null, undefined, symbol
    // object, box container
    // function, first-class function
    
    const count = 17; // integer
    const size = 17.1 // decimal number
    console.log('value: ${count}, type: ${typeof count}'); // value: 17, type: number
    console.log('value: ${count}, type: ${typeof size}');  // value: 17.1, type:number
    
    // number - special numeric values;
    const infinity = 1 / 0; // Infinity
    const negativeInfinity = -1 / 0; // -Infinity
    const nAn = 'not a number' / 2; // NaN
    console.log(infinity);
    console.log(negativeInfinity);
    console.log(nAn);
    
    // bigIn (fairly new, don't use it yet)
    const int = 1234567890123456789012345678901234567890; // over (-2^53 ~ 2^53)
    const bigInt = 1234567890123456789012345678901234567890n; 
    console.log('value: ${bigint}, type: ${typeof bigInt}');
    
    // string
    console char = 'c';
    const brendan = 'brendan';
    const greeting = 'hello' + brendan
    console.log('value: ${greeintg}, type: ${typeof greeting');
    const helloBob = 'h1 ${brendan}!'; // template literals (string
    console.log('value: ${helloBob}, type: ${typeof helloBob}');
    console.log('value: ' + helloBob + ' type: ' + typeof helloBob);
    
    // boolean
    // false:0, null, undefined, Nan, ''
    // true: any other value
    const canRead = true;
    const test = 3 < 1 // false
    console.log('value: ${canRead}, type: $Ptypeof canRead}');
    console.log('value: ${test}, type: ${typeof test}');
    
    // null
    let nothing = null;
    console.log('value: ${nothing}, type: ${typeof nothing}');
    
    // undefined
    let x;
    console.log('value: ${x}, type: ${typeof x}');
    
    // symbol, create unique identifiers for objects
    const symbol1 = Symbol('id');
    const symbol2 = Symbol('id');
    console.log(symbol1 === symbol2); // false
    // 고유한 식별자가 필요하거나, 동시다발적으로 일어나는 코드에서 우선순위를 주고 싶을 때 symbol 활용
    // string은 동일한 string을 썼을 때 같은 식별자로 간주
    // 심볼은 동일한 string을 작성하여도 다른 symbol로 만들어짐
    
    // 동일한 symbol을 만들고 싶은 경우
    const gSymbol1 = Symbol.for('id');
    const gSymbol2 = Symbol.for('id');
    console.log(gSymbol1 === gSymbol2); // true
    console.log('value: ${symbol1.description}, type: ${typeof symbol1}');
    // 심볼은 바로 출력하면 에러가 나기 때문에
    // .dscription을 이용해 string으로 변환하여 출력
    
    // object, real-life object, data strucutre
    const ellie = {name: 'ellie', age: 20};
    ellie.age = 21;
  ```

  <br/>
    
### 📌 Dynamic typing: Dynamically typed language
    
  <br/>

  ```jsx
    let text = 'hello';
    console.log(text.char(0));
    console.log('value: ${text}, type: ${typeof text}'); // value: hello, type: string
    text = 1;
    console.log('value: ${text}, type: ${typeof text'); // value: 1, type: number
    text = '7' + 5;
    console.log('value: ${text}, type: ${typeof text'); // value: 75, type: string
    text = '8' / '2';
    console.log('value: ${text}, type: ${typeof text'); // value: 4, type: number
    console.log(text.charAt(0)); // error
  ```

  <br/>