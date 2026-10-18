### Kamal Mehta

Machine Learning Engineer. I build machine learning that runs in production on 500+ locomotives.

Open to new roles · Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Work

Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026: autonomous freight trains for a Class I U.S. railroad, 500+ locomotives.

| Result | How |
|---|---|
| Raised fuel saving vs manual driving from about 5% to 12% (average across train types) on 1,000+ real trips | [Deep RL Driving Strategy for Freight Trains](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): my DQN model, one 15–20 MB file about 100× smaller than the 2 GB model; EPA-certified for the software in 2025 |
| Replaced per-territory models with 4–6 models covering 120+ territories | [One Model per Train Type](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization): look-ahead terrain features; AWS training cost about 80% lower with RL trained locally |
| Raised simulation precision from 75% to 85% | [Making the Simulator Agree With the Real Train](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): bounded grid search, S3 and Lambda pipeline; precision = 100% minus the 50/50 normalized RMSE of fuel and running time |
| Investigated 100+ client-reported field issues as fleet availability rose from about 90% to 99% | [100+ Field Issues Investigated](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability): root cause and a regression test for each, under a 24-hour SLA |
| Built an Australian client's pipeline from its first 50–100 trips to its pilot and fleet-wide deployment | [The Data Pipeline for an Australian Railroad Client](https://kamal-mehta.com/?r=github#/p/etl-australian-client): two recorders fused into one per-second record on AWS |
| Analyzed 1,000+ real trips to set the fuel targets for the software's 2025 EPA certification | [The Analysis Behind a 12% EPA-Certified Fuel Saving](https://kamal-mehta.com/?r=github#/p/epa-fuel-certification): field analysis, sim-to-field gap fed back |
| Reached 96.25% test accuracy for object detection (MS thesis) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion): YOLOv3 with stereo camera and LiDAR through a Kalman filter; 59 ms detection |

Production code stays private. Public below: a Double DQN eco-driving project in PyTorch and TensorFlow, my MS thesis code in MATLAB, three evaluation kits on invented data with tests and CI, and a design note.

#### Public code

- [dqn-train-energy](https://github.com/kamalkimahek14/dqn-train-energy): Double DQN for fuel-efficient train driving on a simulated track, written in both PyTorch and TensorFlow on one shared environment and training loop; on 50 held-out tracks it used 31.5% less fuel than a speed-holding baseline and arrived on time on 99%.
- [yolov3-camera-lidar-fusion](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): my MS thesis code in MATLAB. Retrains YOLOv3 by transfer learning, calibrates a stereo camera and LiDAR, clusters LiDAR points in a 3D frustum and fuses both positions in a Kalman filter on an unmanned ground vehicle; the thesis reports 96.25% test accuracy and 59 ms detection.
- [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit): scores self-improvement loop rounds on a training panel and a fresh blind panel and flags overfit and stalls; the same method raised my voice assistant's blind pass rate from 47.7% to 77.3%.
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): keeps a site chatbot to published answers with rules and post-checks, tested on a 92-item regression set on an invented persona; the live twin on my site passes 100/100 on its own set.
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness): parses a resume like applicant tracking software and scores it on a company-split held-out set of job posts.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): design of Sarathi, my private local-first AI board: 20 agents and a three-language voice assistant on one laptop GPU; first audio of a three-word reply 1.8 s → 0.3 s (first sentence live in 0.7–1.1 s).

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN, PPO) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · Git · Linux

#### License

Profile text © 2026 Kamal Mehta, [CC BY 4.0](LICENSE).
