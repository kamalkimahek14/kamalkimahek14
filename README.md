### Kamal Mehta

Machine Learning Engineer · Perception Engineer. Deep RL on 500+ locomotives, camera + LiDAR perception, local LLM agents. Open to new roles.

Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Work

Shipped DQN driving models to 500+ autonomous freight locomotives of a Class I U.S. railroad as Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026.

Building Sarathi: 20 local agents and a three-language voice assistant on one 6 GB laptop GPU (design note below). Built Disha, a local career advisor (below).

| Result | How |
|---|---|
| 12% fuel saving vs manual driving, 1,000+ trips (Aug 2024 – Dec 2025); EPA-certified software (2025); under 10 ms per decision, CPU-only | [Deep RL Driving Strategy for Freight Trains](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): my DQN models plus a rule-based refinement layer; one 15–20 MB file per model, about 100× smaller than the 2 GB supervised model |
| Fine-tuned YOLOv3 to test mAP@0.5 96.25%, MS thesis (4 classes; 220 test images, a random 2% frame-level split of the same recordings) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion): YOLOv3 (SqueezeNet backbone) transfer learning on 10,989 labeled images (15,000+ with augmentation); mean IoU 0.82 |
| Cut position error 0.97 m (camera only) → 0.42 m with camera–LiDAR fusion in simulation, with each object's class, MS thesis (LiDAR alone 0.29 m, no class) | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion) · [code](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): YOLOv3 + LiDAR frustum clustering + linear Kalman filter; 1.44 s a frame live on a GTX 1050 (stereo cameras, RealSense L515), 59 ms detection offline |
| 4–6 RL models, one per train type, cover 100+ territories (120 approved) | [One Model per Train Type, Not per Territory](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization): look-ahead terrain features |
| Cut simulator normalized RMSE 0.25 → 0.15 on held-out field trips (random 80/20 split) | [Making the Simulator Agree With the Real Train](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): NRMSE (RMSE/σ, mean of fuel and running time); bounded grid search on field trips; AWS S3/Lambda auto-recalibration |
| Fleet availability about 90% (Jan 2024) → about 99% (Jun 2026) | [100+ Field Issues Investigated](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability): a regression test for each client-reported issue; I wrote an AWS Lambda reliability pipeline and a replacement fleet-health crawler |
| About 8–10% fuel saving in an Australian client's pilot | [The Data Pipeline Behind an Australian Railroad Client's Rollout](https://kamal-mehta.com/?r=github#/p/etl-australian-client): my pipeline, 50–100 trips → fleet-wide; trip analysis fed model updates; ~300-car iron-ore trains, ECP brakes |
| Train consist generation: about 2,500 consists in 4–5 hours instead of about 1 week | [Building Train Make-Ups (Consists) in Parallel](https://kamal-mehta.com/?r=github#/p/consist-generation-scale): Python multiprocessing over OpenSearch |
| About 95–98% wall-position accuracy (within 5 cm) on floor plans from handheld scans at Artifex | [Floor Plans from Handheld Scans](https://kamal-mehta.com/?r=github#/p/floor-plan-generation): density-based clustering separates walls from open space; checked against architects' hand-drawn plans; piloted by about 30 architects |

#### Public code

Production code stays private.

- [dqn-train-energy](https://github.com/kamalkimahek14/dqn-train-energy): Double DQN eco-driving on a simulated train, in PyTorch and TensorFlow. 31.5% less fuel than a speed-holding baseline on 50 evaluation tracks (also used in tuning), on time on 99% (2 seeds); a slack predictor as a safety filter cuts slack events per trip 93% (synthetic data).
- [yolov3-camera-lidar-fusion](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): my 2021 MATLAB thesis pipeline (YOLOv3 transfer learning, camera and LiDAR calibration, Kalman fusion), with 2026 helper scripts. Test mAP@0.5 96.25% (4 classes) in the 2021 thesis; about 1.44 s a frame live on a GTX 1050, 59 ms detection per image offline.
- I wrote [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit) to score loop rounds on a training panel (dev judges) and a fresh blind panel (held-out judges) and flag overfit. I use the same train/held-out method on my voice assistant (held-out pass rate 55.3% → 71.2%, 3-round means).
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): rules and post-checks that keep a site chatbot to published answers, with a 92-item regression set on an invented persona.
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness) parses a resume the way applicant tracking software does. A fuller private version (4 PDF extractors and a port of OpenResume's parser) took my resume's parse score from 85.6% to 100%.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): my current work, a private AI board with 20 agents and a three-language voice assistant on one laptop GPU. TTS synthesis latency (three-word reply): 1.8 s → 0.3 s after moving the voice to the GPU; time to first audio (first sentence, timed live): 0.7–1.1 s.

#### Disha, a local career advisor (private repo, code on request)

I built Disha (Hindi for "direction") to score a resume, LinkedIn profile, GitHub profile and portfolio site separately, out of 100, against live postings for one target role, with strict title matching and skill gaps taken from the requirements 15%+ of companies name.

- It shows a recruiter's ATS view and rewrites in the user's own words as a diff; a number they never wrote becomes [N].
- For each top match it writes a tailored resume and cover letter (PDF, DOCX, Markdown), plus a print-ready report and a week-by-week roadmap.
- Everything runs on 127.0.0.1 with a local Ollama reviewer; CI runs 617 tests on Python 3.11 and 3.13 and a PII scan.
- Review rounds R19–R24 with invented job seekers and recruiters took usefulness from 5.0 to 7.0 and credibility from 6.75 to 8.0 (out of 10).

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN; PPO explored as a baseline) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering · LiDAR and stereo camera calibration · ROS · Gazebo
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · AWS CodePipeline · GitHub Actions · Git · Linux

#### License

Profile text © 2026 Kamal Mehta, [CC BY 4.0](LICENSE).
