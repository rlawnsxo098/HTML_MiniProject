# HTML_MiniProject

## ๐ฅ Team Members
###  ๊น์์ง
  * ๋ก๊ทธ์ธ, ํํ์ด์ง, ์ํ, ํ์๊ฐ์ ๋ฑ ์ ์ ๋ฐ ์ค๊ณ

###  ๊น์คํ
  * ์ฃผ๋ฌธ, ์ํ ๋ฑ ์ ์ ๋ฐ ์ค๊ณ
 
###  ๊น์ํ
  * ๊ฒ์ํ๋ฉด ๋ฐ ๊ฒ์ ์์ง ์ ์ ๋ฐ ์ค๊ณ


## ๐ซ Language
<p>
 <img src="https://img.shields.io/badge/HTML5-E34F26?&style=flat-square&logo=html5&logoColor=white"/> 
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" /> 
<img src="https://img.shields.io/badge/JavaScript-323330?style=flat-square&logo=javascript&logoColor=F7DF1E" />
 </p>

## โญSource Code

### 'ํ์๊ฐ์.js'
```
function checkValidPassword(form) {
    if (form.password.value == "") {
        document.getElementById('alert_password').innerText = "๋น๋ฐ๋ฒํธ๋ฅผ ๋ค์ ์๋ ฅํ์ธ์";
        //form.password.focus();
        return false;
    }

    const pw = form.password.value;
    // String.prototype.search() ๊ฒ์๋ ๋ฌธ์์ด ์ค์ ์ฒซ ๋ฒ์งธ๋ก ๋งค์น๋๋ ๊ฒ์ ์ธ๋ฑ์ค๋ฅผ ๋ฐํ. ์ฐพ์ง ๋ชปํ๋ฉด -1 ์ ๋ฐํ
    // number
    const num = pw.search(/[0-9]/g);
    // alphabet
    const eng = pw.search(/[a-z]/ig);
    // special characters
    const spe = pw.search(/[`~!@@#$%^&*|โฉโฉโฉ'โฉ";:โฉ/?]/gi);

    if (pw.length < 6) {
        // ์ต์ 6๋ฌธ์.
        document.getElementById('alert_password').innerText = "๋น๋ฐ๋ฒํธ๋ 6์๋ฆฌ ์ด์์ด์ด์ผ ํฉ๋๋ค";
        return false;
    } else if (pw.search(/\s/) != -1) {
        // ๊ณต๋ฐฑ ์ ๊ฑฐ.
        document.getElementById('alert_password').innerText = "๋น๋ฐ๋ฒํธ์ ๊ณต๋ฐฑ์ด ์์ด์ผ ํฉ๋๋ค";
        return false;
    } else if (num < 0 && eng < 0 && spe < 0) {
        // ํ๊ธ๊ณผ ๊ฐ์ ๋ฌธ์์ด ์๋ ฅ ๋ฐฉ์ง.
        document.getElementById('alert_password').innerText = "๋น๋ฐ๋ฒํธ๋ก ์ฌ์ฉํ  ์ ์์ต๋๋ค";
        return false;
    }

    return true;
}
```

### 'product.js'
 
```
function carousel() {
    var i;
    var x = document.getElementsByClassName("mySlides");
    
    for (i = 0; i < x.length; i++) {
      x[i].style.display = "none";
    }
    slideIndex++;
    if (slideIndex > x.length) {slideIndex = 1}
    x[slideIndex-1].style.display = "block";
    setTimeout(carousel, 3000); // Change image every 2 seconds
}
```

### 'orderScript.js'
```
function plusTable1(){
    const costValue = document.querySelector("#value");
    let row_3 = document.createElement('tr');
    let row_3_data_1 = document.createElement('td');
    var x = document.createElement("IMG");
    x.setAttribute("src", img2);
    x.setAttribute("width", 200);
    x.setAttribute("height", 200);

    row_3_data_1.innerHTML = x;
    let row_3_data_2 = document.createElement('td');
    row_3_data_2.innerHTML = product;
    let row_3_data_3 = document.createElement('td');
    row_3_data_3.innerHTML =price;

    costValue.textContent = price;
    row_3.appendChild(x);
    row_3.appendChild(row_3_data_2);
    row_3.appendChild(row_3_data_3);
    tbody.appendChild(row_3);
}
```

## โ๏ธ Review

### node.js๋ฅผ ์ด์ฉํ์ฌ Open API, Get, Post ๋ฐฉ์์ผ๋ก ๋ฐ์ดํฐ๋ฅผ ์ ์กํ์ฌ ์์ฑ๋๋ฅผ ๋์ด๋ฉฐ
### ๊ตฌํํ๊ณ ์ ํ๋ ๋ด์ฉ์ ๊ตฌํํ  ์์ ์ด๋ค.
### ํ์๋ถ๋ค์ด ๋๋ฌด ์ํด์ฃผ์์ ํธํ๊ฒ ์งํํ  ์ ์์๋ค.


 


