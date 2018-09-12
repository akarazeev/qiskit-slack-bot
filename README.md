# qiskit-bot

Bots that use Qiskit

# QuantumComputingBot <img src="img/rqc.png" href='http://rqc.ru/' width='15%' align='right'>

Monitoring the load of IBM Q processors from [IBM Quantum Experience](https://quantumexperience.ng.bluemix.net) (data for 24 hours).

| Calibration for [IBM QX 4](https://github.com/QISKit/ibmqx-backend-information/tree/master/backends/ibmqx4/V1) | Pending jobs for [IBM QX 5](https://github.com/QISKit/ibmqx-backend-information/blob/master/backends/ibmqx5/README.md)     |
| :------------- | :------------- |
| <img src="img/errors_demo.png" width="200px">       | <img src="img/jobs_demo.png" width="400px">       |

### Bot for Slack

Bot is already available inside [QISKit](https://qiskit.org) workspace in [Slack](https://slack.com).<img src="img/qiskit-logo-black.png" href='http://rqc.ru/' width='7%' align='right'><img src="img/slack.png" href='http://rqc.ru/' width='7%' align='right'>

Bot understands the following commands:

* `/full [backend]` - calibration and pending jobs info for backend
* `/gate_errors [backend]` - send gate errors
* `/jobs [backend]` - diagram of pending jobs
* `/readout_errors [backend]` - send readout errors

`backend` is the name for quantum processors like [ibmqx4](https://github.com/QISKit/ibmqx-backend-information/tree/master/backends/ibmqx4/V1) or [ibmqx5](https://github.com/QISKit/ibmqx-backend-information/blob/master/backends/ibmqx5/README.md).

| Step 1 | Step 2 | Step 3 |
| :-------------: | :-------------: | :-------------: |
| <img src="img/slack_1.jpg" width="200px">       | <img src="img/slack_2.jpg" width="200px">       | <img src="img/slack_3.jpg" width="200px">       |

| Pass backend as argument - 1 | Pass backend as argument - 2 |
| :-------------: | :-------------: |
| <img src="img/slack_jobs_1.jpg" width="200px">       | <img src="img/slack_jobs_2.jpg" width="200px">       |


## Description

Structure of the project:
```
...
├── main_slack.py          <- Slack bot.
├── main_dumper.py         <- Crawler that dumps statistics
|                             into pickled data.
├── utils.py               <- File with methods for plotting.
├── data                   <- Folder with pickled data.
│   ├── real_data_1.pkl
│   └── ...
├── img                    <- Images for this README.
│   ├── jobs_demo.jpg
│   └── ...
├── res                    <- Folder with different resource files
|   |                         including tokens for APIs.
│   ├── rqc.jpg
│   ├── token_q.json
│   └── ...
└── tmp                    <- Folder with generated plots.
    ├── ibmqx4_full.png
    └── ...
```


## Authors

🇦🇺🇷🇺[Yaroslav Kharkov](https://www.physics.unsw.edu.au/staff/yaroslav-kharkov) &lt;[y.kharkov@gmail.com](mailto:y.kharkov@gmail.com)&gt;, [Anton Karazeev](https://akarazeev.github.io) &lt;[anton.karazeev@gmail.com](mailto:anton.karazeev@gmail.com)&gt;
