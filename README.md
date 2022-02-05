# korean-nli-datasets

데이콘의 [한국어 문장 관계 분류 경진대회 대회](https://dacon.io/competitions/official/235875/overview/description)를 참여하면서 NLI 데이터셋 특징을 정리하고 이용 상 불편함을 해결하고자 리포지토리 생성


## [KorNLI](https://github.com/kakaobrain/KorNLUDatasets)
변경사항
- 탭 구분자가 인식되지 않는 문제가 있음. SNLI, XNLI에서 구분되지 않는 행을엑셀로 값을 수정함

데이터셋 특징
- MNLI : 기계번역으로 인해 n/a나 제대로 번역되지 않고 정제되지 않은 값이 많음
- SNLI : 
- XNLI : 


## [KLUE-NLI](https://github.com/KLUE-benchmark/KLUE)
변경사항
- json 파일을 단순히 CSV 파일로 변경

데이터셋 특징
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
