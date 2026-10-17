### Kamal Mehta

Machine Learning Engineer. I build machine learning that runs in production.

Open to new roles · Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Work

Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026: autonomous freight trains for a Class I U.S. railroad, 500+ locomotives.

| Result | How |
|---|---|
| Raised fuel saving vs manual driving from about 5% to 12% (average across train types) on 1,000+ real trips; one 15–20 MB DQN package, about 100× smaller than the 2 GB model | [Deep RL Driving Strategy for Freight Trains](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): built the DQN model and slack predictor that run on all 500+ locomotives; the EPA certified the 12% for the software in 2025 |
| Replaced per-territory models with 4–6 models covering 120+ territories | [One Model per Train Type](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization): look-ahead terrain features;; AWS training cost about 80% lower with RL trained locally |
| Raised simulation precision from 75% to 85% | [Simulator Calibration](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): bounded grid search, S3 and Lambda pipeline; precision = 100% minus the 50/50 normalized RMSE of fuel and running time |
| Investigated 100+ client-reported field issues as fleet availability rose from about 90% to 99% | [100+ Field Issues Investigated](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability): root cause and a regression test for each, under a 24-hour SLA |
| Built an Australian client's pipeline from its first 50–100 trips to its pilot and fleet-wide deployment | [Australian Client Pipeline](https://kamal-mehta.com/?r=github#/p/etl-australian-client): two recorders fused into one per-second record on AWS |
| Analyzed 1,000+ real trips to set the fuel targets for the software's 2025 EPA certification | [EPA Fuel Analysis](https://kamal-mehta.com/?r=github#/p/epa-fuel-certification): field analysis, sim-to-field gap fed back |
| Classified 96% of test objects correctly (MS thesis) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion): YOLOv3 with stereo camera and LiDAR through a Kalman filter; 59 ms detection |

Production code stays private; the public kits below are my code on invented data.

#### Now

- [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit): scores self-improvement loop rounds with a training panel and a fresh blind panel, and flags overfit and stalls; the same method raised my voice assistant's blind pass rate from 47.7% to 77.3%.
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): the rules and post-checks behind my site twin, with a 92-item regression set on an invented persona (32 trick questions, 20 model-reply checks); my site twin passes its own separate 100-item set.
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness): the standard-library core of my resume test harness: ATS-style parse, skill coverage and a company-split held-out set with a separation proof, on an invented resume.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): design note for Sarathi, my private local-first AI board: 20 agents and a three-language voice assistant on one laptop GPU; first audio 1.8 s → 0.3 s.

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN, PPO) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · Git · Linux

## License

This profile text is © 2026 Kamal Mehta, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it with credit to Kamal Mehta. The full text is in [LICENSE](LICENSE).
