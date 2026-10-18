### Kamal Mehta

Machine Learning Engineer. I built machine learning that runs in production on 500+ locomotives.

Open to Machine Learning Engineer, Forward Deployed Engineer and Applied AI Engineer roles · Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Public code

Production code stays private.

- [dqn-train-energy](https://github.com/kamalkimahek14/dqn-train-energy): Double DQN eco-driving on a simulated train, in PyTorch and TensorFlow. 31.5% less fuel than a speed-holding baseline on 50 held-out tracks, on time on 99%; speed-limit overshoots (0.31 per trip) are the next fix.
- [yolov3-camera-lidar-fusion](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): MS thesis code in MATLAB (2021 scripts, 2026 helpers): YOLOv3 transfer learning, camera and LiDAR calibration, Kalman fusion. 96.25% mAP@0.5 (4 classes), 59 ms detection.
- [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit): scores loop rounds on a training panel and a fresh blind panel, and flags overfit. I use the same train/held-out method on my voice assistant (held-out pass rate 47.7% → 77.3%).
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): rules and post-checks that keep a site chatbot to published answers, with a 92-item regression set on an invented persona.
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness): parses a resume the way applicant tracking software does. A fuller private version with 5 extractors took my resume's parse score from 85.6% to 100%.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): my current work, a private AI board with 20 agents and a three-language voice assistant on one laptop GPU. Text-to-speech time to first audio for a three-word reply: 1.8 s → 0.3 s.

#### Work

Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026: autonomous freight trains for a Class I U.S. railroad, 500+ locomotives.

| Result | How |
|---|---|
| Raised fuel saving vs manual driving from about 5% to 12% on 1,000+ real trips with my DQN models (unit and mixed-freight trains) | [Deep RL Driving Strategy for Freight Trains](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): each a 15–20 MB file, about 100× smaller than the 2 GB model; EPA-certified for the software in 2025 |
| Replaced per-territory models with 4–6 models covering 120+ territories | [One Model per Train Type](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization): look-ahead terrain features; AWS training cost about 80% lower with RL trained locally |
| Raised simulation fidelity from 75% to 85% | [Making the Simulator Agree With the Real Train](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): bounded grid search, S3 and Lambda pipeline; fidelity = 100% minus the 50/50 normalized RMSE of fuel and running time |
| Investigated 100+ client-reported field issues as fleet availability rose from about 90% (Jan 2024) to about 99% (mid-2026) | [100+ Field Issues Investigated](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability): root cause and a regression test for each, under a 24-hour SLA; my crawler add-on, deployed in May–June 2026, helped close the gap |
| Built an Australian client's pipeline from its first 50–100 trips to fleet-wide deployment; trip analysis from it fed model updates that reached about 8–10% fuel saving in the pilot | [The Data Pipeline for an Australian Railroad Client](https://kamal-mehta.com/?r=github#/p/etl-australian-client): ~300-car iron-ore trains with ECP brakes; two recorders fused into one per-second record on AWS; separate from the EPA-certified 12% |
| Cut train consist generation from about a week to 4–5 hours | [Building Train Make-Ups (Consists) in Parallel](https://kamal-mehta.com/?r=github#/p/consist-generation-scale): about 2,500 per run with Python multiprocessing over OpenSearch |
| Analyzed 1,000+ real trips to set the fuel targets for the software's 2025 EPA certification | [The Analysis Behind a 12% EPA-Certified Fuel Saving](https://kamal-mehta.com/?r=github#/p/epa-fuel-certification): field analysis, sim-to-real gap fed back |
| Reached a test mAP@0.5 of 96.25% (4 classes) for object detection (MS thesis) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion): YOLOv3 with stereo camera and LiDAR through a Kalman filter; 59 ms detection |

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN, PPO) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · Git · Linux

#### License

Profile text © 2026 Kamal Mehta, [CC BY 4.0](LICENSE).
