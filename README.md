<p align="center">
    <img src=".github/logo.png" alt="Stego Tool Logo" width="620"/>
</p>

### A Command-Line System Guardian by **Fossil Logic**

Stego Tool is a powerful **system monitoring and diagnostics utility** designed for administrators, developers, and performance engineers who demand deep visibility into their systems. It provides comprehensive insight into hardware, processes, system health, and security—consolidated into a single, cohesive command-line interface.

Unlike traditional tools that only expose fragments of system state, Stego delivers **holistic system intelligence** with commands like `profile` for full system overviews, `pulse` for real-time monitoring, and `analyze` for AI-assisted diagnostics.

---

## Features

- **Full system profiling** — Inspect CPU, memory, disk, GPU, firmware, and network in one unified view
- **Real-time system monitoring** — Track system health with live metrics and visualizations
- **Deep inspection tools** — Analyze processes, threads, memory regions, and hardware components
- **System call tracing** — Observe kernel-level activity and performance behavior
- **Security and configuration audits** — Detect misconfigurations, vulnerabilities, and risks
- **Thermal and pressure monitoring** — Track temperatures and system resource contention
- **Snapshot and diff system states** — Capture and compare system states over time
- **Advanced logging tools** — Query, filter, and stream system logs
- **AI-assisted diagnostics** — Detect bottlenecks, anomalies, and optimization opportunities
- **Enhanced shell introspection** — Extended `env`, `echo`, and `process` analysis tools

---

## **Why Choose Stego Tool?**

Stego Tool acts as the **defensive backbone** of your system toolkit—providing clarity, stability, and control in complex environments.

- **Holistic Visibility**: View your entire system—from hardware to processes—in one place.
- **Beyond Traditional Tools**: Combines functionality of `top`, `htop`, `lsof`, `dmesg`, and more into a unified interface.
- **Proactive Diagnostics**: Identify issues before they become critical with forecasting and anomaly detection.
- **Security Awareness**: Built-in auditing and inspection for system hardening.
- **Developer & Admin Focused**: Designed for those who need deep insight without juggling multiple utilities.
- **Cross-Platform**: Works seamlessly across Linux, macOS, and Windows.
- **Modern & Extensible**: Built for performance with a modular architecture.

Stego Tool is your **system’s shield**—always watching, always ready.

---

## **Prerequisites**

Ensure you have the following installed before starting:

- **Meson Build System**: This project relies on Meson. For installation instructions, visit the official [Meson website](https://mesonbuild.com/Getting-meson.html).

## **Setting Up Meson Build**

1. **Install Meson**:
    - Follow the installation guide on the [Meson website](https://mesonbuild.com/Getting-meson.html) for your operating system.

## **Setting Up, Compiling, Installing, and Running the Project**

1. **Clone the Repository**:

    ```sh
    git clone https://github.com/fossillogic/stego.git
    cd stego
    ```

2. **Configure the Build**:

    ```sh
    meson setup builddir
    ```

3. **Compile the Project**:

    ```sh
    meson compile -C builddir
    ```

4. **Install the Project**:

    ```sh
    meson install -C builddir
    ```

5. **Run the Project**:

    ```sh
    stego --help
    ```

## Command Palette

---

### System Intelligence & Monitoring

| **Command** | **Description** | **Flags** |
|-------------|-----------------|-----------|
| `profile` | Display a comprehensive system profile (CPU, memory, disk, OS, firmware, network, GPU). | `--cpu`<br>`--memory`<br>`--disk`<br>`--gpu`<br>`--network`<br>`--firmware`<br>`--all`<br>`--json`<br>`--lookup <key>` |
| `pulse` | Real-time system health monitor (enhanced top/htop). | `--interval <n>`<br>`--cpu`<br>`--mem`<br>`--disk`<br>`--net`<br>`--thermal`<br>`--top`<br>`--graph` |
| `inspect` | Deep inspection of system components. | `--cpu`<br>`--core <id>`<br>`--process <pid>`<br>`--thread`<br>`--memory-region`<br>`--device <name>` |
| `trace` | Trace system calls or kernel activity. | `--pid <id>`<br>`--syscalls`<br>`--signals`<br>`--io`<br>`--time`<br>`--summary` |
| `audit` | Run diagnostics and detect misconfigurations. | `--security`<br>`--permissions`<br>`--services`<br>`--startup`<br>`--integrity`<br>`--report <file>` |
| `watchsys` | Monitor system events in real-time. | `--events <list>`<br>`--interval <n>`<br>`--threshold <value>`<br>`--alert` |
| `thermals` | Monitor temperatures and cooling systems. | `--cpu`<br>`--gpu`<br>`--fan`<br>`--interval <n>`<br>`--alert <temp>` |
| `pressure` | Measure system pressure (CPU, memory, IO contention). | `--cpu`<br>`--memory`<br>`--io`<br>`--duration <n>`<br>`--graph` |
| `uptime` | Show uptime and load averages. | `--since`<br>`--load`<br>`--pretty` |
| `limits` | Display system resource limits. | `--user`<br>`--process`<br>`--open-files`<br>`--stack` |
| `devices` | List and inspect hardware devices. | `--usb`<br>`--pci`<br>`--block`<br>`--tree`<br>`--details` |
| `drivers` | Show loaded drivers/modules. | `--list`<br>`--info <name>`<br>`--dependencies` |
| `services` | Manage and inspect system services. | `--list`<br>`--status <name>`<br>`--start`<br>`--stop`<br>`--restart`<br>`--logs` |
| `logs` | Query and filter system logs. | `--since <time>`<br>`--until <time>`<br>`--level <type>`<br>`--follow`<br>`--grep <pattern>` |
| `snapshot` | Capture full system state. | `--name <label>`<br>`--diff <other>`<br>`--compress`<br>`--include <component>` |
| `diffsys` | Compare system states. | `--cpu`<br>`--memory`<br>`--disk`<br>`--services`<br>`--json` |
| `forecast` | Predict system resource trends. | `--cpu`<br>`--memory`<br>`--disk`<br>`--window <time>`<br>`--model <type>` |
| `analyze` | AI-assisted diagnostics and insights. | `--bottleneck`<br>`--anomaly`<br>`--optimize`<br>`--summary` |
| `secure` | Inspect system security posture. | `--firewall`<br>`--users`<br>`--permissions`<br>`--open-ports`<br>`--vuln` |
| `entropy` | Monitor entropy/randomness pool. | `--rate`<br>`--pool`<br>`--alert <threshold>` |

---

### Extended Shell Introspection

| **Command** | **Description** | **Flags** |
|-------------|-----------------|-----------|
| `echo+` | Enhanced echo with formatting and diagnostics. | `--color`<br>`--format <type>`<br>`--escape`<br>`--analyze` |
| `env+` | Advanced environment variable inspector. | `--list`<br>`--diff <snapshot>`<br>`--export <file>`<br>`--filter <pattern>`<br>`--source` |
| `process+` | Advanced process explorer. | `--tree`<br>`--top`<br>`--filter <name>`<br>`--sort <key>`<br>`--kill <pid>`<br>`--trace` |
| `who` | Show active users and sessions. | `--sessions`<br>`--history`<br>`--ip` |
| `caps` | Display system capabilities and features. | `--cpu-flags`<br>`--virtualization`<br>`--security` |
| `pathing` | Inspect executable resolution paths. | `--which <cmd>`<br>`--all`<br>`--order` |

---

### Global Flags

| **Flag** | **Description** |
|-----------|-----------------|
| `--help` | Show command help. |
| `--version` | Display Spino Tool version. |
| `-v, --verbose` | Enable detailed output. |
| `-q, --quiet` | Suppress standard output. |
| `--dry-run` | Simulate actions without changes. |
| `--color` | Colorize output where applicable. |
| `--time` | Display timestamps in output. |

---

### Usage Examples

| **Example** | **Description** |
|---|---|
| `stego profile --all` | Display full system profile. |
| `stego profile --lookup cpu.cores` | Query a specific system property. |
| `stego pulse --cpu --mem --interval 1` | Real-time CPU and memory monitoring. |
| `stego inspect --process 1337` | Inspect a specific process. |
| `stego trace --pid 1337 --syscalls` | Trace system calls for a process. |
| `stego audit --security --report audit.json` | Run a security audit and export results. |
| `stego thermals --cpu --alert 85` | Monitor CPU temperature with alert threshold. |
| `stego logs --level error --follow` | Stream system error logs. |
| `stego snapshot --name baseline` | Capture system snapshot. |
| `stego diffsys --cpu --memory` | Compare system states. |
| `stego analyze --bottleneck` | Detect performance bottlenecks. |
| `stego env+ --diff baseline.env` | Compare environment variables. |

---

## **Contributing**

Interested in contributing? Please open pull requests or create issues on the [GitHub repository](https://github.com/fossillogic/stego).

## **Feedback and Support**

For issues, questions, or feedback, open an issue on the [GitHub repository](https://github.com/fossillogic/stego/issues).

## **License**

This project is licensed under the [Apache Public License](LICENSE).
