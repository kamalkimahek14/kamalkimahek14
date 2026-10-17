### Kamal Mehta

Machine Learning Engineer. I build machine learning that runs in production.

Open to new roles · Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Work

Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026: autonomous freight trains for a Class I U.S. railroad, 500+ locomotives.

| Result | How |
|---|---|
| Raised fuel saving vs manual driving from about 5% to 12% on 1,000+ real trips, the figure the EPA certified for the software in 2025 | [Deep RL driving](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): moved a 2 GB tree ensemble to a DQN model in PyTorch; my DQN model and slack predictor ship on all 500+ locomotives |
| Replaced the 2 GB model with one 15–20 MB DQN package, about 100× smaller | [One file per locomotive](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): the model, its features and its processing, on the onboard computer |
| Replaced per-territory models with 4–6 models covering 120+ territories | [Look-ahead terrain features](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization); AWS training cost about 80% lower with RL trained locally |
| Raised simulation precision from 75% to 85% | [Simulator calibration](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): bounded grid search, S3 and Lambda pipeline; precision = 100% minus the 50/50 normalized RMSE of fuel and running time |
| Investigated 100+ client-reported field issues as fleet availability rose from about 90% to 99% | [Root cause, then a regression test for each](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability) |
| Built an Australian client's pipeline from its first 50–100 trips to fleet-wide deployment | [Two recorders fused into one per-second record on AWS](https://kamal-mehta.com/?r=github#/p/etl-australian-client) |
| Analyzed 1,000+ real trips to set the fuel targets for the software's 2025 EPA certification | [Field analysis, sim-to-field gap fed back](https://kamal-mehta.com/?r=github#/p/epa-fuel-certification) |
| Classified 96% of test objects correctly (MS thesis) | [YOLOv3 with stereo camera and LiDAR through a Kalman filter](https://kamal-mehta.com/?r=github#/p/perception-fusion); 59 ms detection |

Production code stays private; the public kits below are my code on invented data.

#### Now

- [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit): scores self-improvement loop rounds with a training panel and a fresh blind panel, and flags overfit and stalls; the same method raised my voice assistant's blind pass rate from 47.7% to 77.3%.
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): the rules and post-checks behind my site twin, with a 92-item regression set on an invented persona (32 trick questions, 20 bad model replies).
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness): the standard-library core of my resume test harness: ATS-style parse, skill coverage and a company-split held-out set with a separation proof, on an invented resume.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): design note for Sarathi, my private local-first AI board: 20 agents and a three-language voice assistant on one laptop GPU.

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN, PPO) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · Git · Linux

## License

This profile text is © 2026 Kamal Mehta, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it with credit to Kamal Mehta. The full text is in [LICENSE](LICENSE).
