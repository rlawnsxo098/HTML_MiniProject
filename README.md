# HTML_MiniProject

## 🥇 Team Members
###  김예지
  * 로그인, 홈페이지, 상품, 회원가입 등 제작 및 설계

###  김준태
  * 주문, 상품 등 제작 및 설계
 
###  김은혁
  * 검색화면 및 검색 엔진 제작 및 설계


## 💫 Language
<p>
 <img src="https://img.shields.io/badge/HTML5-E34F26?&style=flat-square&logo=html5&logoColor=white"/> 
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" /> 
<img src="https://img.shields.io/badge/JavaScript-323330?style=flat-square&logo=javascript&logoColor=F7DF1E" />
 </p>

## ⭐Source Code

### '회원가입.js'
```
function checkValidPassword(form) {
    if (form.password.value == "") {
        document.getElementById('alert_password').innerText = "비밀번호를 다시 입력하세요";
        //form.password.focus();
        return false;
    }

    const pw = form.password.value;
    // String.prototype.search() 검색된 문자열 중에 첫 번째로 매치되는 것의 인덱스를 반환. 찾지 못하면 -1 을 반환
    // number
    const num = pw.search(/[0-9]/g);
    // alphabet
    const eng = pw.search(/[a-z]/ig);
    // special characters
    const spe = pw.search(/[`~!@@#$%^&*|₩₩₩'₩";:₩/?]/gi);

    if (pw.length < 6) {
        // 최소 6문자.
        document.getElementById('alert_password').innerText = "비밀번호는 6자리 이상이어야 합니다";
        return false;
    } else if (pw.search(/\s/) != -1) {
        // 공백 제거.
        document.getElementById('alert_password').innerText = "비밀번호에 공백이 없어야 합니다";
        return false;
    } else if (num < 0 && eng < 0 && spe < 0) {
        // 한글과 같은 문자열 입력 방지.
        document.getElementById('alert_password').innerText = "비밀번호로 사용할 수 없습니다";
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

## ☀️ Review

### node.js를 이용하여 Open API, Get, Post 방식으로 데이터를 전송하여 완성도를 높이며
### 구현하고자 하는 내용을 구현할 예정이다.
### 팀원분들이 너무 잘해주셔서 편하게 진행할 수 있었다.


 


