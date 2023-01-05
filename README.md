# Node.js Homework_1

<details close>
<summary> Question_1 and Answer</summary> </br>

Hepimizin Matematik derslerinden bildiği üzere Dairenin Alanı = π x r2 şeklinde hesaplanır. Node.JS Javascript çalışma ortamında yarıçap değerini konsoldan parametre olarak girerek alanı bulmaya çalışacağız.
Konsol çıktısı: Yarıçapı (Yarıçap) olan dairenin alanı: (Alan) şeklinde olmalıdır.

```javascript
const arguments = process.argv;
arguments[2]*=1;

function zone(r){
    pi = 3;
    return pi*(r**2)
}
zone = zone(arguments[2]);

console.log("Yarıçapı",arguments[2], "olan dairenin alanı :" , zone);

```

![](https://github.com/MehmetMaytahan/Kodluyoruz_NodeJs_Repo/blob/main/question_1.png)

</details>

# Node.js Homework_2

<details close>
<summary> Question_2 and Answer </summary> </br>

Blog oluşturmaya hazır mısınız? Konsol ekranında postlarımızı sıralayalım, sonrasında yeni bir post oluşturalım ve yeni post ile birlikte postlarımızı tekrar sıralayalım.

```js
const posts = [
  { title: "Post One", body: "This is post one" },
  { title: "Post Two", body: "This is post two" },
  { title: "Post Three", body: "This is post three" }
];

const listPosts = () => {
  posts.map(p => {
    console.log(p.title);
  });
};

const addPost = (newPost, callback) => {
  posts.push(newPost);
  callback();
};

addPost({ title: "Post Four", body: "This is post four" }, listPosts);


```

![](https://github.com/MehmetMaytahan/Kodluyoruz_NodeJs_Repo/blob/main/question_2.png)

</details>

# Node.js Homework_3

<details close>

  <summary>Question_3 and Answer</summary>
  
  1. Daire alan : circleArea ve daire çevre : circleCircumference fonksiyonları içeren ve consola sonuçları
  yazdıran circle.js dosyası oluşturunuz.
  2. Module.exports yöntemi ile fonksiyonları oluştururken export ediniz.
  3. require ve object destructing kullanarak index.js dosyasında yarıçap (r) 5 olacak şekilde ekran çıktısını alınız.

  ```js
  // circle.js
  
  const circleArea = r => {
    return Math.PI *r* r;
  };

  const circleCircumference = r => {
    return 2 *Math.PI* r;
  };

  module.exports = {
    circleArea,
    circleCircumference
  };

  ```

  ```js
  // index.js
  
  const { circleArea, circleCircumference } = require("./circleModule/circle");

  console.log(`Circle area: ${circleArea(5)}`);
  console.log(`Circle Circumference: ${circleCircumference(5)}`);
  ```

  ![](https://github.com/MehmetMaytahan/Kodluyoruz_NodeJs_Repo/blob/main/question_3.png)


</details>

# Node.js Homework_4

<details close>
  <summary>Question_4 and Answer</summary>

```js
import { readFile, writeFile, rm } from "fs";

const file = "employees.json";
const data = `{"name": "Employee 1 Name", "salary": 2000}`;
const updateData = `{"name": "Employee 2 Name", "salary": 5000}`;
const format = "utf-8";

// DOSYA YAZMA
const _writeFile = () => {
  writeFile(file, data, format, err => {
    if (err) throw err;
    console.log("Dosya yazma islemi basarili: ", JSON.parse(data));
  });
};

// DOSYA OKUMA
const _readFile = () => {
  readFile(file, format, (err, data) => {
    if (err) throw err;
    console.log("Dosya okuma islemi basarili: ", JSON.parse(data));
  });
};

// DOSYA GUNCELLEME
const _updateFile = () => {
  writeFile(file, updateData, format, err => {
    if (err) throw err;
    console.log("Dosya guncelleme islemi basarili: ", JSON.parse(updateData));
  });
};

// DOSYA SILME
const _deleteFile = () => {
  rm(file, { recursive: true }, err => {
    if (err) throw err;
    console.log("Dosya silme islemi basarili: ", "employees.json");
  });
};

const operations = [_writeFile, _readFile, _updateFile, _deleteFile];
operations.map(operation => operation());
```

![](https://github.com/MehmetMaytahan/Kodluyoruz_NodeJs_Repo/blob/main/question_4.png)

</details>



***

## License

[MIT](https://choosealicense.com/licenses/mit/)
