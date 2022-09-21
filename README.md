# Introduction
웹사이트 반응형 페이지
* Component Language : Html,css,JavaScript,
* design : Photoshop

# Description
메인페이지

# Creation Period
2022-08-18 ~ 08-21
# finished version
![KCC글라스_main](https://user-images.githubusercontent.com/102776957/191405784-163ab39e-6bc8-4011-b0c7-967e47939566.jpg)

# Features
* Swiper parallax

# Development(Main Page Important part)
* 페럴렉스 넘어갈때 애니메이션 추가 삭제 반복 
```C
      const mainSwiper = new Swiper("#main", {
        direction: "vertical",
        speed: 1000,
        parallax: true,
        mousewheel: true,
        // touchRatio: 0,
        pagination: {
          el: ".wrap .pagination",
          type: "progressbar",
        },
        on: {
          slideChangeTransitionEnd: function () {},
          slidePrevTransitionStart: function () {
            console.log("올라감");
            setTimeout(classChange, 600);
          },
          slideNextTransitionStart: function () {
            console.log("내려감");
            setTimeout(classChange, 600);
          },
        },
      });

      function classChange() {
        if (mainSwiper.realIndex === 1) {
          for (blueColor of blue) {
            blueColor.classList.add("open");
          }
          for (beigeColor of beige) {
            beigeColor.classList.remove("open");
          }
        } else if (mainSwiper.realIndex === 2) {
          for (beigeColor of beige) {
            beigeColor.classList.add("open");
          }
          for (blueColor of blue) {
            blueColor.classList.remove("open");
          }
        } else {
          for (beigeColor of beige) {
            beigeColor.classList.remove("open");
          }
          for (blueColor of blue) {
            blueColor.classList.remove("open");
          }
        }
      }
```
