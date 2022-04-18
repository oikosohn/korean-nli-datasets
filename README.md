# 한국어 NLI 데이터셋 모음 (Korean NLI Datasets)

데이콘의 [한국어 문장 관계 분류 경진대회 대회](https://dacon.io/competitions/official/235875/overview/description)를 참여하면서 확인한 한국어 NLI 데이터셋 특징을 정리하였습니다. 또 데이터셋을 이용하면서 겪은 불편함을 해결하고자 저장소를 생성하였습니다. 


## [KorNLI](https://github.com/kakaobrain/KorNLUDatasets)

엑셀에서 KorNLI 데이터셋의 값을 확인하려면 UTF-8로 로드해야합니다.

### 변경사항
- [탭 구분자가 인식되지 않는 문제](https://github.com/kakaobrain/KorNLUDatasets/issues/4)가 있음. SNLI, XNLI에서 구분되지 않는 행을 엑셀로 값을 수정하였습니다.
- MNLI는 탭 구분이 인식되지 않는 행이 매우 많아서 **수정하지 않고 업로드하였습니다.** MNLI를 이용할 때 pandas의 read_csv의 skiprows를 사용해야 합니다.


### 데이터셋 특징

기계번역을 거쳤기 때문에 한국어에서 자주 쓰이지 않는 관사(`그`), 지시사(`이것`, `저것`, `그것` 등)가 많습니다.
- MNLI : 기계 번역으로 △ 제대로 번역되지 않고 △ 정제되지 않은 값(`n/a`, `의성어`, `의태어`)이 많음. 
- SNLI : 기계 번역이지만 제대로 번역된 값이 대다수임. 원본이 이미지 캡션에 기반한 문장 쌍이라서 대체로 장면 묘사가 많음.
- XNLI : 기계 번역 후 전문 번역가가 편집. dev와 test 데이터로 구분됨. 인명 표기가 한국어와 영어로 표시되어 있음.
  - `xnli_test.csv`, `xnli_dev.csv` 데이터셋의 전제(premise, sentence1) 문장의 인명이 한글로 번역되어있는 반면에 가설(hypothesis, sentence2) 문장은 영어로 표기되어 있는 경우가 있습니다. 아래는 `xnli_test.csv`에서 찾은 한 가지 예시입니다.
    
    ```
    - 전제 문장 : 데이비슨은 스콘의 발음을 '뼈'와 운을 맞추기 위해 채택해서는 안 된다.
    - 가설 문장 : Davidson은 스콘과 뼈가 운을 맞춰야 한다고 믿지 않는다.
    ```

## [KLUE-NLI](https://github.com/KLUE-benchmark/KLUE)
### 변경사항
- 엑셀 상에서 값을 확인하기 위해서 json 파일 확장자를 단순히 csv 파일로 변경하였습니다.


### 데이터셋 특징
- KLUE NLI 1.1 버전 
- 자연스러운 한국어 문장 데이터셋
- 데이터 출처 : 네이버 영화 리뷰(NSMC), 에어비앤비 리뷰(airbnb), 위키트리(wikitree), 정책 뉴스 브리핑 자료(policy), 위키뉴스(wikinews), 위키피디아(wikipedia) 
  - train 구성 : 24998 문장
    | 출처 |  문장 개수 | 비율 |
    | --- | ---: | ---: |
    | 네이버 영화 리뷰(NSMC) | 4899 | 0.196 |
    | 에어비앤비 리뷰(airbnb) | 4824 | 0.193 | 
    | 위키트리(wikitree) | 3838 | 0.153 | 
    | 정책 뉴스 브리핑 자료(policy) | 3833 | 0.153 |
    | 위키뉴스(wikinews) | 3824 | 0.153 |
    | 위키피디아(wikipedia) | 3780| 0.151 |
  - dev 구성 : 3000 문장
    | 출처 |  문장 개수 | 비율 |
    | --- | ---: | ---: |
    | 네이버 영화 리뷰(NSMC) | 600 | 0.20 |
    | 에어비앤비 리뷰(airbnb) | 600 | 0.20 | 
    | 위키트리(wikitree) | 450 | 0.15 | 
    | 정책 뉴스 브리핑 자료(policy) | 450 | 0.15 |
    | 위키뉴스(wikinews) | 450 | 0.15 |
    | 위키피디아(wikipedia) | 450| 0.15 |

## License
License for KorNLI and KLUE NLI datasets
- [Creative Commons Attribution-ShareAlike license (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/)



## References
```bibtex
@article{ham2020kornli,
  title={KorNLI and KorSTS: New Benchmark Datasets for Korean Natural Language Understanding},
  author={Ham, Jiyeon and Choe, Yo Joong and Park, Kyubyong and Choi, Ilji and Soh, Hyungjoon},
  journal={arXiv preprint arXiv:2004.03289},
  year={2020}
}

@misc{park2021klue,
      title={KLUE: Korean Language Understanding Evaluation},
      author={Sungjoon Park and Jihyung Moon and Sungdong Kim and Won Ik Cho and Jiyoon Han and Jangwon Park and Chisung Song and Junseong Kim and Yongsook Song and Taehwan Oh and Joohong Lee and Juhyun Oh and Sungwon Lyu and Younghoon Jeong and Inkwon Lee and Sangwoo Seo and Dongjun Lee and Hyunwoo Kim and Myeonghwa Lee and Seongbo Jang and Seungwon Do and Sunkyoung Kim and Kyungtae Lim and Jongwon Lee and Kyumin Park and Jamin Shin and Seonghyun Kim and Lucy Park and Alice Oh and Jungwoo Ha and Kyunghyun Cho},
      year={2021},
      eprint={2105.09680},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
