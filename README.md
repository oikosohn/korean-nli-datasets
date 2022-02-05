# korean-nli-datasets

데이콘의 [한국어 문장 관계 분류 경진대회 대회](https://dacon.io/competitions/official/235875/overview/description)를 참여하면서 한국어 NLI 데이터셋 특징을 정리하고 이용 상 불편함을 해결하고자 리포지토리 생성

## [KorNLI](https://github.com/kakaobrain/KorNLUDatasets)
### 변경사항
- [탭 구분자가 인식되지 않는 문제](https://github.com/kakaobrain/KorNLUDatasets/issues/4)가 있음. SNLI, XNLI에서 구분되지 않는 행을 엑셀로 값을 수정함

- MNLI는 탭 구분이 인식되지 않는 행이 매우 많아서 보류


<!---
  | | 예시 문장 | 변경된 예시 문장 |
  | --- | --- | --- |
  | 전제 문장 | 데이비슨은 스콘의 발음을 '뼈'와 운을 맞추기 위해 채택해서는 안 된다. | 없음 |
  | 가설 문장 | Davidson은 스콘과 뼈가 운을 맞춰야 한다고 믿지 않는다. | 데이비슨은 스콘과 뼈가 운을 맞춰야 한다고 믿지 않는다. |

--->

### 데이터셋 특징

기계번역을 거쳤기 때문에 한국어에서 자주 쓰이지 않는 관사(`그`), 지시사(`이것`, `저것`, `그것` 등)가 많음

데이터셋의 전제(premise, sentence1) 문장의 인명이 한글로 번역되어있는 반면에 가설(hypothesis, sentence2) 문장은 영어로 표기되어 있는 경우 있음

- MNLI : 기계 번역으로 △ 제대로 번역되지 않고 △ 정제되지 않은 값(`n/a`, `의성어`, `의태어`)이 많음

- SNLI : 

- XNLI : 기계 번역 후 전문 번역가가 편집


## [KLUE-NLI](https://github.com/KLUE-benchmark/KLUE)
### 변경사항
- json 파일을 단순히 CSV 파일로 변경

### 데이터셋 특징
- KLUE-NLI : 


## License
[Creative Commons Attribution-ShareAlike license (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/)
- License for KorNLI and KLUE NLI datasets


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
