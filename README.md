### Kamal Mehta

Machine Learning Engineer · Perception Engineer. Deep RL on 500+ locomotives, camera + LiDAR perception, local LLM agents. Open to new roles.

Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Work

Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026: autonomous freight trains for a Class I U.S. railroad, 500+ locomotives.

Current work: Sarathi, a private, local-first AI board with 20 agents and a three-language voice assistant on one 6 GB laptop GPU (design note below).

| Result | How |
|---|---|
| 12% fuel saving vs manual driving, 1,000+ trips (Aug 2024 – Dec 2025); EPA-certified software (2025) | [Deep RL Driving Strategy for Freight Trains](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): my DQN models plus a rule-based refinement layer; one 15–20 MB file per model, about 100× smaller than the 2 GB supervised model; under 10 ms per decision, CPU-only. |
| Camera–LiDAR fusion, MS thesis: mean position error 0.97 m (camera alone) → 0.42 m fused in simulation (LiDAR alone 0.29 m, no class) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion) · [code](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): YOLOv3; LiDAR points clustered in each box's 3D frustum; Kalman fusion; about 1.44 s a frame live (GTX 1050), 59 ms detection offline |
| Detection, MS thesis: test mAP@0.5 96.25% (4 classes; random 2% frame-level test split of the same recordings) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion): YOLOv3 (SqueezeNet backbone) transfer learning on 10,989 labeled images; mean IoU 0.82 |
| 4–6 per-train-type RL models replace per-territory models; 100+ territories run RL (120+ approved; pilot ~6–7) | [One Model per Train Type, Not per Territory](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization): look-ahead terrain features |
| Simulator normalized RMSE 0.25 → 0.15 on held-out field trips | [Making the Simulator Agree With the Real Train](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): NRMSE (RMSE/σ, mean of fuel and running time); bounded grid search on field trips; AWS S3/Lambda auto-recalibration |
| Fleet availability about 90% (Jan 2024) → about 99% (mid-2026) | [100+ Field Issues Investigated](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability): a regression test for each client-reported issue; my replacement crawler helped close the gap |
| About 8–10% fuel saving in an Australian client's pilot | [The Data Pipeline Behind an Australian Railroad Client's Rollout](https://kamal-mehta.com/?r=github#/p/etl-australian-client): my pipeline, 50–100 trips → fleet-wide; trip analysis fed model updates; ~300-car iron-ore trains, ECP brakes |
| Train consist generation: about a work week → 4–5 hours | [Building Train Make-Ups (Consists) in Parallel](https://kamal-mehta.com/?r=github#/p/consist-generation-scale): Python multiprocessing over OpenSearch |
| About 95–98% wall-position accuracy (within 5 cm) on floor plans from handheld scans at Artifex | [Floor Plans from Handheld Scans](https://kamal-mehta.com/?r=github#/p/floor-plan-generation): density-based clustering separates walls from open space; checked against architects' hand-drawn plans; piloted by about 30 architects |

#### Public code

Production code stays private.

- [dqn-train-energy](https://github.com/kamalkimahek14/dqn-train-energy): Double DQN eco-driving on a simulated train, in PyTorch and TensorFlow. 31.5% less fuel than a speed-holding baseline on 50 test tracks (the tracks were also read between tuning rounds), on time on 99%; a slack predictor as a safety filter cuts slack events per trip 93% (synthetic data); speed-limit violations (0.31 per trip) are the next fix.
- [yolov3-camera-lidar-fusion](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): MS thesis code in MATLAB (2021 scripts, 2026 helpers): YOLOv3 transfer learning, camera and LiDAR calibration, Kalman fusion. Test mAP@0.5 96.25% (4 classes) in the 2021 thesis; about 1.44 s a frame live on a GTX 1050, 59 ms detection per image offline. The rewritten training code runs in MATLAB R2026b: a 1,000-iteration pipeline check on a 548-image sample reached test mAP@0.5 0.46 (a pipeline check, not the thesis model).
- [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit): scores loop rounds on a training panel (dev judges) and a fresh blind panel (held-out judges), and flags overfit. I use the same train/held-out method on my voice assistant (held-out pass rate 55.3% → 71.2%, 3-round means).
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): rules and post-checks that keep a site chatbot to published answers, with a 92-item regression set on an invented persona.
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness): parses a resume the way applicant tracking software does. A fuller private version (4 PDF extractors and a port of OpenResume's parser) took my resume's parse score from 85.6% to 100%.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): my current work, a private AI board with 20 agents and a three-language voice assistant on one laptop GPU. TTS synthesis latency (three-word reply): 1.8 s → 0.3 s after moving the voice to the GPU; time to first audio (first sentence, timed live): 0.7–1.1 s.

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN; PPO explored as a baseline) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · AWS CodePipeline · GitHub Actions · Git · Linux

#### License

Profile text © 2026 Kamal Mehta, [CC BY 4.0](LICENSE).
