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
![](https://github.com/MehmetMaytahan/Kodluyoruz_NodeJs_Repo/blob/main/quesion1.png)

</details>

***

## License

[MIT](https://choosealicense.com/licenses/mit/)