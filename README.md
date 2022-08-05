# KoreArch : 고고학 관련 R 패키지 한국어 번역 프로젝트

 KoreArch는 고고학 연구에 활용되는 R 패키지들의 `README`, `Vignette` 등을 한국어로 번역하여 공유하고자 시작된 프로젝트입니다. 결론적으로 이를 통해 R에 대한 한국인 고고학 연구자들의 접근성을 높히고, 이에 대한 관심을 증진시키고자 합니다.

 번역은 패키지를 제작한 집단 혹은 개인에게 허락을 구하고 이루어졌습니다.

## 패키지 목록

 패키지명을 누르면 번역된 패키지의 `README`를 확인할 수 있습니다.

-   [oxcAAR](https://github.com/ChanToRe/oxcAAR/blob/master/README_ko.md) : `oxcAAR`은 `OxCal`을 R에서 사용하기 위한 함수들이 내장된 패키지로 [ISAAK](https://isaakiel.github.io/)에 의해 관리되고 있습니다. `OxCal`은 고고학 연구에서 활용되는 방사성탄소연대에 대한 일종의 준표준격의 프로그램으로 `oxcAAR`을 통해 R내에서 사용할 수 있습니다.

## 패키지 일괄 설치

`AllPkgInstall.R`을 통해 목록의 패키지들을 일괄적으로 설치할 수 있습니다. 번역된 패키지들이 추가될 때마다 업데이트 됩니다. (최근 : 2022/08/05)

    all_pkg <- function(pkg){
      new.pkg <- pkg[!(pkg %in% installed.packages()[, "Package"])]
      if (length(new.pkg))
        install.packages(new.pkg, dependencies = TRUE)
      sapply(pkg, require, character.only = TRUE)
    }

    pkg_list <- c("oxcAAR", "Bchron", "rcarbon")

    all_pkg(pkg_list)

## 기여 및 문의

 KoreArch에 대한 기여는 누구나 언제든지 할 수 있습니다. 기여는 번역, 디자인 등 다양한 형태로 이루어질 수 있습니다. KoreArch 레포지토리를 `Fork`하여 작업한 후 `Pull-Request`를 해주세요. 검토 후 병합하겠습니다.

 문의는 `Issue`에 남겨주시거나 [E-mail](mailto:chanhyeok@soongsil.ac.kr)로 보내주세요.
