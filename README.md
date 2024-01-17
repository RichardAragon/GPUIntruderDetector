**GPU Intruder Detector**

**Overview**

This program monitors GPU memory usage and alerts users when potential anomalies are detected. It's designed to help identify issues such as memory leaks or unexpected behavior in GPU-intensive workloads, particularly those involving large language models (LLMs).

**Features**

- Continuously monitors GPU memory usage.
- Detects significant changes in memory usage that might indicate anomalies.
- Sends email alerts when anomalies are detected.
- Logs events, anomalies, and errors for analysis.
- Supports NVIDIA and AMD GPUs.
- Configurable via environment variables.

**Installation**

1. **Prerequisites:**
    - Python 3.6 or later
    - NVIDIA GPU: `nvidia-smi` tool
    - AMD GPU: `rocminfo` tool (optional)
    - Email server for sending alerts (if desired)

**Usage**

1. **Set environment variables (optional):**
   - `MONITORING_INTERVAL`: Interval between checks in seconds (default: 60)
   - `THRESHOLD`: Threshold for triggering anomaly alerts (default: 0.8)
   - `SMTP_SERVER`: SMTP server for email alerts
   - `SMTP_PORT`: SMTP server port
   - `EMAIL_ADDRESS`: Email address to send alerts from
   - `EMAIL_PASSWORD`: Password for the email address
   - `TO_EMAILS`: Comma-separated list of recipient email addresses

**Configuration**

- Adjust the `MONITORING_INTERVAL` and `THRESHOLD` variables as needed.
- Configure email settings if you want to receive alerts.

**License**

This program is released under the MIT open source license.

**Author**

Richard Aragon

**Contributing**

Pull requests are welcome!

**Troubleshooting**

- Check the `gpu_monitor.log` file for errors or debugging information.
- Ensure you have the correct GPU tools installed (`nvidia-smi` or `rocminfo`).
- Verify your email server configuration if alerts aren't being sent.

**Additional Notes**

- Consider integrating this tool with other monitoring frameworks or dashboards.
- Explore adding support for more GPU metrics (e.g., temperature, power consumption).
- Experiment with different threshold values to fine-tune anomaly detection.
