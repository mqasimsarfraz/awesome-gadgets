# Awesome Gadgets [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome gadgets and resources for [Inspektor Gadget](https://www.inspektor-gadget.io/).

[Inspektor Gadget](https://www.inspektor-gadget.io/) is a framework for creating, publishing, and sharing eBPF gadgets.

## Contents

- [Official Resources](#official-resources)
- [Official Gadgets](#official-gadgets)
- [Community Gadgets](#community-gadgets)
- [Libraries & Tools](#libraries--tools)
- [Gadget Development](#gadget-development)
- [Talks](#talks)
- [Blogs & Articles](#blogs--articles)
- [Community](#community)

## Official Resources

- [Inspektor Gadget Documentation](https://inspektor-gadget.io/docs/latest/)
- [Inspektor Gadget GitHub](https://github.com/inspektor-gadget/inspektor-gadget)
- [Inspektor Gadget Website](https://inspektor-gadget.io/docs/latest/)

## Official Gadgets

### Advise

- [advise_networkpolicy](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/advise_networkpolicy) - Monitors network activity and records TCP/UDP traffic summaries to generate Kubernetes network policies.
- [advise_seccomp](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/advise_seccomp) - Records syscalls issued in a container to generate seccomp profiles.

### Audit

- [audit_seccomp](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/audit_seccomp) - Provides a stream of events with syscalls that had their access denied by seccomp policies.

### Profile

- [profile_blockio](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/profile_blockio) - Profiles the block I/O of a node.
- [profile_cpu](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/profile_cpu) - Profiles the CPU.
- [profile_cuda](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/profile_cuda) - Profiles CUDA memory allocations.
- [profile_qdisc_latency](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/profile_qdisc_latency) - Profiles the latency of the network scheduler on a node.
- [profile_tcprtt](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/profile_tcprtt) - Profiles TCP connections' Round-Trip Time (RTT).

### Snapshot

- [snapshot_file](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/snapshot_file) - Gathers information about all open files (regular and directories by default).
- [snapshot_process](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/snapshot_process) - Shows running processes.
- [snapshot_socket](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/snapshot_socket) - Gathers information about TCP and UDP sockets.

### Top

- [top_blockio](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/top_blockio) - Provides a periodic list of input/output block device activity (requires Linux Kernel 6.5+).
- [top_cpu_throttle](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/top_cpu_throttle) - Periodically reports CFS CPU bandwidth throttling statistics per cgroup.
- [top_cuda_memory](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/top_cuda_memory) - Periodically reports CUDA memory allocation and free activity per process.
- [top_file](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/top_file) - Reports periodically the read/write activity by file.
- [top_process](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/top_process) - Periodically reports process statistics including CPU and memory usage.
- [top_tcp](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/top_tcp) - Reports periodically TCP send/receive activity by connection.

### Trace

- [trace_bind](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_bind) - Streams socket binding syscalls.
- [trace_capabilities](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_capabilities) - Shows what capability security checks are triggered by applications.
- [trace_dns](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_dns) - Traces DNS queries and responses.
- [trace_exec](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_exec) - Notifies when new processes are executed.
- [trace_fsslower](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_fsslower) - Streams file operations (open, read, write, and fsync) that are slower than a threshold.
- [trace_init_module](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_init_module) - Emits events when processes invoke `init_module()` or `finit_module()` syscalls to load kernel modules.
- [trace_lsm](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_lsm) - Notifies for LSM tracepoints.
- [trace_malloc](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_malloc) - Traces malloc and free in libc using uprobes.
- [trace_mount](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_mount) - Traces mount and unmount events.
- [trace_oomkill](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_oomkill) - Traces OOM kill events.
- [trace_open](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_open) - Emits events when files are opened.
- [trace_signal](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_signal) - Traces signals.
- [trace_sni](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_sni) - Traces Server Name Indication (SNI) from TLS requests.
- [trace_ssl](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_ssl) - Captures data on read/write functions of OpenSSL, GnuTLS, NSS, and Libcrypto.
- [trace_tcp](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_tcp) - Tracks TCP connect, accept, and close.
- [trace_tcpdrop](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_tcpdrop) - Tracks TCP drop events.
- [trace_tcpretrans](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/trace_tcpretrans) - Tracks TCP retransmissions.

### Other

- [bpfstats](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/bpfstats) - Provides statistics about memory and CPU usage for BPF programs.
- [deadlock](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/deadlock) - Traces pthread mutex lock/unlock to detect potential deadlocks.
- [fdpass](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/fdpass) - Traces file descriptor passing via a unix socket (`SCM_RIGHTS`).
- [fsnotify](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/fsnotify) - Detects applications using inotify or fanotify.
- [tcpdump](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/tcpdump) - Captures packets in container contexts with pcap-compatible filters.
- [traceloop](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/traceloop) - Syscalls flight recorder.
- [ttysnoop](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/gadgets/ttysnoop) - Watches the output from a tty or pts device.

## Community Gadgets

- [kubescape/node-agent gadgets](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets) - Security-focused eBPF gadgets used by the Kubescape node agent for runtime threat detection. Includes the following gadgets:
  - [exit](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/exit) - Traces process exit events with exit code, signal, and overlayfs detection.
  - [fork](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/fork) - Traces process fork events and reports parent/child process identifiers.
  - [hardlink](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/hardlink) - Traces hardlink creation syscalls (link, linkat) for auditing hardlink operations.
  - [http](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/http) - Monitors HTTP traffic by intercepting syscalls and capturing request/response payloads.
  - [iouring_new](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/iouring_new) - Traces io_uring submit events for kernel >= 6.4.
  - [iouring_old](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/iouring_old) - Traces io_uring submit events for kernel < 6.3.
  - [kmod](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/kmod) - Monitors kernel module loading via init_module and finit_module syscalls.
  - [network](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/network) - Traces network connection attempts (TCP/UDP) with source/destination details.
  - [ptrace](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/ptrace) - Traces ptrace syscalls that modify target memory/registers for injection detection.
  - [randomx](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/randomx) - Detects RandomX cryptocurrency mining activity by monitoring FPU register patterns.
  - [ssh](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/ssh) - Detects SSH connections by scanning TCP payload for SSH protocol signatures.
  - [symlink](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/symlink) - Traces symlink creation syscalls to detect suspicious symlink operations.
  - [unshare](https://github.com/kubescape/node-agent/tree/main/pkg/ebpf/gadgets/unshare) - Monitors unshare syscalls to track namespace unsharing operations.
- [micromize](https://github.com/micromize-dev/micromize) - Kernel-enforced boundary hardening for cloud-native containers using BPF-LSM. Includes the following gadgets:
  - [binary-attestation](https://github.com/micromize-dev/micromize/tree/main/gadgets/binary-attestation) - Attests binary and shared object integrity using IMA file hashes.
  - [cap-restrict](https://github.com/micromize-dev/micromize/tree/main/gadgets/cap-restrict) - Restricts privileged capabilities.
  - [fs-restrict](https://github.com/micromize-dev/micromize/tree/main/gadgets/fs-restrict) - Restricts filesystem boundaries.
  - [ptrace-restrict](https://github.com/micromize-dev/micromize/tree/main/gadgets/ptrace-restrict) - Restricts ptrace-based debugging/injection attacks.
- [trace-ktls](https://github.com/dorser/trace-ktls) - Captures plaintext from kTLS connections using eBPF by hooking kernel TLS ULP functions.
- [trace-udns](https://github.com/alban/trace-udns) - Detects DNS requests using uprobes.
- [syscall-profiler-gadget](https://github.com/dorser/syscall-profiler-gadget) - Collects count metrics for selected syscalls called within containers.
- [signal-go-gadget](https://github.com/alban/signal-go-gadget) - Sends signals to Go processes to capture goroutine stack traces on specific syscalls.
- [runc-vuln-detector](https://github.com/alban/runc-vuln-detector) - Detects and mitigates runc vulnerabilities (CVE-2024-21626, CVE-2025-31133, CVE-2025-52881).

## Libraries & Tools

- [ig-mcp-server](https://github.com/inspektor-gadget/ig-mcp-server) - MCP server that bridges Inspektor Gadget's eBPF observability with LLMs for AI-powered root cause analysis of Kubernetes and Linux issues.
- [ig-desktop](https://github.com/inspektor-gadget/ig-desktop) - Desktop application for Inspektor Gadget built with Wails and Svelte, available for Windows, Mac, and Linux.
- [ig-extcap](https://github.com/inspektor-gadget/ig-extcap) - Wireshark extcap plugin for capturing container-aware network traffic using the Inspektor Gadget tcpdump gadget.
- [headlamp-plugin](https://github.com/inspektor-gadget/headlamp-plugin) - Headlamp UI plugin for visualizing and managing Inspektor Gadget data in a Kubernetes dashboard.
- [charts](https://github.com/inspektor-gadget/charts) - Helm charts for deploying Inspektor Gadget on Kubernetes clusters.

## Gadget Development

- [gadget-template](https://github.com/inspektor-gadget/gadget-template) - Template repository for creating custom Inspektor Gadget gadgets with eBPF and OCI packaging.
- [Building a Gadget](https://www.inspektor-gadget.io/docs/latest/gadget-devel/building) - Official guide on building and packaging gadgets as OCI images.
- [Gadget Development Documentation](https://www.inspektor-gadget.io/docs/latest/gadget-devel/) - Comprehensive documentation for developing custom gadgets.
- [Inspektor Gadget Go Package](https://pkg.go.dev/github.com/inspektor-gadget/inspektor-gadget) - Go library for embedding Inspektor Gadget functionality in Go applications.
- [setup-ig](https://github.com/mqasimsarfraz/setup-ig) - GitHub Action to install the `ig` in CI/CD workflows.
- [build-push-gadget](https://github.com/mqasimsarfraz/build-push-gadget) - GitHub Action to build, push, and optionally sign gadget OCI images with cosign.

## Talks

- **[OpenSearch Con NA 2025 - From Kernel To Cloud: Building a Complete Open Source Observability Pipeline](https://opensearchconna2025.sched.com/event/25Gp0/from-kernel-to-cloud-building-a-complete-open-source-observability-pipeline-anirudha-jadhav-shenoy-pratik-gurudatt-amazon-web-services)** - Anirudha Jadhav Shenoy, Pratik Gurudatt ([video](https://www.youtube.com/watch?v=oWZnSS7mtK4), [slides](https://static.sched.com/hosted_files/opensearchconna2025/a8/From%20Kernel%20To%20Cloud_%20Building%20a%20Complete%20Open%20Source%20Observability%20Pipeline_final.pdf))
- **[Container Days Hamburg 2024 - Demystifying DNS: A Guide to Understanding and Debugging Request Flows in Kubernetes Clusters](https://www.youtube.com/watch?v=KQpZg_NqbZw)**
- **[eBPF Data Collection for Everyone – empowering the community to obtain Linux insights using Inspektor Gadget](https://www.youtube.com/watch?v=tkKXdaqji9c)**

## Blogs & Articles

- [Results from the First Inspektor Gadget Security Audit](https://www.inspektor-gadget.io/blog/2026/04/inspektor-gadget-security-audit) - Brian Benz, Francis Laniel - Walkthrough of the first independent security audit by Shielder/OSTIF.
- [Visualize gadget data with the Inspektor Gadget plugin for Headlamp](https://www.inspektor-gadget.io/blog/2025/03/inspektor-gadget-plugin-for-headlamp) - Visualizing gadget data using the Headlamp Kubernetes UI plugin.
- [Announcing the Deprecation of Built-In Gadgets](https://www.inspektor-gadget.io/blog/2025/02/deprecation-built-in-gadgets) - Maya Singh - Migration guide from built-in to image-based gadgets.
- [Introducing a new gadget for detecting deadlocks](https://www.inspektor-gadget.io/blog/2024/12/deadlock-gadget-lfx-mentorship) - Snehil Shah - Deadlock detection gadget built during LFX mentorship.
- [Debugging DNS with Inspektor Gadget](https://www.inspektor-gadget.io/blog/2024/11/inspektor-gadget-dns) - Qasim Sarfraz - DNS debugging techniques using IG.
- [Inspektor Gadget at Cloud Native Rejekts and KubeCon NA 2024!](https://www.inspektor-gadget.io/blog/2024/10/inspektor-gadget-kubecon-na) - Recap of IG at KubeCon NA 2024.
- [Introduction to Gadgets](https://www.inspektor-gadget.io/blog/2024/09/introduction-to-gadgets) - Mauricio Vásquez Bernal - Comprehensive introduction to the gadget concept.
- [Empowering Observability: The Advent of Image-Based Gadgets](https://www.inspektor-gadget.io/blog/2024/08/empowering-observability_the_advent_of_image_based_gadgets) - Chris Kühl - Deep dive into the image-based gadget architecture.

## Community

- [Slack](https://kubernetes.slack.com/messages/inspektor-gadget/)

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
