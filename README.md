### Kamal Mehta

Machine Learning Engineer. I built machine learning that runs in production on 500+ locomotives.

Open to Machine Learning Engineer and Perception Engineer roles · Dallas–Fort Worth, TX · kamalmehta.ai@gmail.com

[kamal-mehta.com](https://kamal-mehta.com/?r=github) · [Ask my digital twin](https://kamal-mehta.com/chat/?r=github) · [LinkedIn](https://www.linkedin.com/in/kamal-m-3ba627b4/)

#### Work

Machine Learning Engineer at Progress Rail (Caterpillar), 2022–2026: autonomous freight trains for a Class I U.S. railroad, 500+ locomotives.

| Result | How |
|---|---|
| 5% → 12% fuel saving vs manual driving on 1,000+ trips (Aug 2024 – Dec 2025) with my DQN models (reward shaping toward a rule-based reference driver on ~2k synthetic trips) and a rule-based refinement layer, EPA-certified for the software in 2025 | [Deep RL Driving Strategy for Freight Trains](https://kamal-mehta.com/?r=github#/p/deep-rl-driving): each model one 15–20 MB file, about 100× smaller than the 2 GB one |
| 4–6 models, one per train type, replaced per-territory models: supervised pilot 2 → ~6–7 territories, RL 100+ (120+ approved) | [One Model per Train Type, Not per Territory](https://kamal-mehta.com/?r=github#/p/feature-engineering-generalization): look-ahead terrain features |
| Normalized RMSE (RMSE/σ; equal-weighted mean of fuel and running time) 0.25 → 0.15 on held-out field trips | [Making the Simulator Agree With the Real Train](https://kamal-mehta.com/?r=github#/p/train-physics-calibration): fit to field trips with a bounded grid search; an AWS S3 and Lambda pipeline recalibrates it as new trips land |
| 100+ client-reported field issues investigated as fleet availability rose from about 90% (Jan 2024) to about 99% (mid-2026) | [100+ Field Issues Investigated](https://kamal-mehta.com/?r=github#/p/rca-fleet-availability): a regression test for each; my replacement crawler helped close the gap |
| An Australian client's pipeline, first 50–100 trips to fleet-wide; its trip analysis fed model updates that reached about 8–10% fuel saving in the client's pilot | [The Data Pipeline Behind an Australian Railroad Client's Rollout](https://kamal-mehta.com/?r=github#/p/etl-australian-client): ~300-car iron-ore trains with ECP brakes |
| Fuel targets from 1,000+ real trips behind the EPA-certified 12%; analyses for directors and the SVP of Advanced Technology | [The Analysis Behind a 12% Fuel Saving, Certified by the EPA](https://kamal-mehta.com/?r=github#/p/epa-fuel-certification): field logs of about 1 TB a day (2026) feed the analysis |
| Week-long backend tasks done in ½–1 day with GitHub Copilot and spec-driven AI coding agents; a self-serve Talos message formatter | [Agentic Software Engineering](https://kamal-mehta.com/?r=github#/p/agentic-ai-coding): I write the spec, AI coding agents implement it, tests gate each merge |
| Train consist generation: about a work week → 4–5 hours | [Building Train Make-Ups (Consists) in Parallel](https://kamal-mehta.com/?r=github#/p/consist-generation-scale): Python multiprocessing over OpenSearch |
| Floor plans from handheld scans at Artifex: about 95–98% wall-position accuracy against architects' hand-drawn plans, piloted by about 30 architects | [Floor Plans from Handheld Scans](https://kamal-mehta.com/?r=github#/p/floor-plan-generation): density-based clustering separates walls from open space |
| Test mAP@0.5 96.25% (4 classes) for object detection, MS thesis | [MS Thesis](https://kamal-mehta.com/?r=github#/p/perception-fusion): YOLOv3 with stereo camera and LiDAR through a Kalman filter |

#### Public code

Production code stays private.

- [dqn-train-energy](https://github.com/kamalkimahek14/dqn-train-energy): Double DQN eco-driving on a simulated train, in PyTorch and TensorFlow. 31.5% less fuel than a speed-holding baseline on 50 test tracks, on time on 99%; a slack predictor as a safety filter cuts slack events per trip 93% (synthetic data); speed-limit violations (0.31 per trip) are the next fix.
- [yolov3-camera-lidar-fusion](https://github.com/kamalkimahek14/yolov3-camera-lidar-fusion): MS thesis code in MATLAB (2021 scripts, 2026 helpers): YOLOv3 transfer learning, camera and LiDAR calibration, Kalman fusion. 96.25% mAP@0.5 (4 classes) in the 2021 thesis, with the rewritten training code verified end to end in MATLAB R2026b; 59 ms detection.
- [eval-loop-kit](https://github.com/kamalkimahek14/eval-loop-kit): scores loop rounds on a training panel (dev judges) and a fresh blind panel (held-out judges), and flags overfit. I use the same train/held-out method on my voice assistant (held-out pass rate 55.3% → 71.2%, 3-round means).
- [twin-eval-kit](https://github.com/kamalkimahek14/twin-eval-kit): rules and post-checks that keep a site chatbot to published answers, with a 92-item regression set on an invented persona.
- [resume-ats-harness](https://github.com/kamalkimahek14/resume-ats-harness): parses a resume the way applicant tracking software does. A fuller private version (4 PDF extractors and a port of OpenResume's parser) took my resume's parse score from 85.6% to 100%.
- [sarathi-design-note](https://github.com/kamalkimahek14/sarathi-design-note): my current work, a private AI board with 20 agents and a three-language voice assistant on one laptop GPU. Text-to-speech time to first audio for a three-word reply: 1.8 s → 0.3 s.

#### Stack

- Python · PyTorch · TensorFlow · scikit-learn · pandas · NumPy · SQL · C++ · Cython · MATLAB
- Reinforcement learning (DQN, PPO) · supervised learning · unsupervised learning (clustering) · computer vision (YOLOv3, CNNs) · sensor fusion and Kalman filtering
- LLMs · RAG · local agents (Ollama) · Cloudflare Workers AI
- AWS (S3, Lambda, QuickSight, OpenSearch) · Docker · AWS CodePipeline · GitHub Actions · Git · Linux

#### License

Profile text © 2026 Kamal Mehta, [CC BY 4.0](LICENSE).
