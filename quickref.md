| Process |
|---------|
| pidof <PROCESS> |
| ps -fp <PID> |
| lsof -p <PID> |
| ps aux |
| ps -ef |
| pgrep -a <PROCESS> |

| Networking |
|------------|
| netstat -natp |
| lsof -i :<PORT> |

| Security |
|----------|
| strace -p <PID> |
| strace -c <PROCESS> |
| getcap <PROCESS_PATH> |
| getpcaps <PID> |

| Directories |
|-------------|
| /var/lib/kubelet/seccomp/profile |
| /var/log/ |
| /etc/kubernetes/manifests/ |
| /etc/apt/source.list.d/kubernetes |
| /etc/sysctl.d/.conf |

| Debug |
|-------|
| k debug node/<NODE_NAME> -it --image=busybox |
| k get --raw "/api/v1/nodes/<NODE_NAME>/proxy/stats/summary" |
| k debug <NAME> -it --image=busybox --target <CONTAINER_NAME> -n <NAMESPACE> |
| journalctl -u kubelet --no-pager |
| cat /usr/include/asm*/unistd* |

| AppArmor |
|-------|
| systemctl status apparmor|
| cat /sys/module/apparmor/parameters/enabled |
| cat /sys/kernel/security/apparmor/profiles |
| apt-get install -y apparmor-utils |
| aa-status |
| aa-genprof <SCRIPT_PATH> |
| /etc/apparmor.d/ |
| appaprmor_parser |
