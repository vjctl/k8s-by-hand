| Process |
|---------|
| pidof <PROCESS> |
| ps -fp <PID> |
| lsof -p <PID> |
| ps -aux |

| Networking |
|------------|
| netstat -natp |
| lsof -i :<PORT> |

| Security |
|----------|
| strace -p <PID> |
| strace -c <PROCESS> |

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
