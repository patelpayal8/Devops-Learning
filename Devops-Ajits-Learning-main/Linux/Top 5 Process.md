
# ✅ Top 5 CPU & Memory -Consuming Processes

@patelpayal8 ➜ /workspaces/Devops-Learning (main) $ ps -eo pid,ppid,cmd,%cpu,%mem --sort=-%mem | head -n 6

    PID    PPID CMD                         %CPU %MEM
    590     569 /vscode/bin/linux-x64/2901c 58.0 14.4
   2136     590 /vscode/bin/linux-x64/2901c 54.9  2.7
    569     560 /vscode/bin/linux-x64/2901c 10.7  2.3
   1011     569 /vscode/bin/linux-x64/2901c  1.8  0.8
     57       1 dockerd --dns 168.63.129.16  0.6  0.8



@patelpayal8 ➜ /workspaces/Devops-Learning (main) $ ps aux | awk 'NR>1 {print $0 | "sort -k4 -nr"}' | head -n 5

codespa+     590 24.7 12.2 65851412 999512 ?     Sl   09:01   0:21 /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/node --dns-result-order=ipv4first /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/out/bootstrap-fork --type=extensionHost --transformURIs --useHostProxy=false
codespa+    2136  9.1  5.3 12997932 433772 ?     Sl   09:01   0:05 /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/node /home/codespace/.vscode-remote/extensions/ms-python.vscode-pylance-2025.6.2/dist/server.bundle.js --cancellationReceive=file:242b90db177092fa4a1c15f7dda0350c05977db877 --node-ipc --clientProcessId=590
codespa+     569  3.7  1.4 11833164 114016 ?     Sl   09:01   0:03 /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/node /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/out/server-main.js --log trace --force-disable-user-env --server-data-dir /home/codespace/.vscode-remote --accept-server-license-terms --host 127.0.0.1 --port 0 --connection-token-file /home/codespace/.vscode-remote/data/Machine/.connection-token-2901c5ac6db8a986a5666c3af51ff804d05af0d4 --extensions-download-dir /home/codespace/.vscode-remote/extensionsCache --start-server  --enable-remote-auto-shutdown --skip-requirements-check
codespa+     603  8.4  1.1 1261952 93508 ?       Sl   09:01   0:07 /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/node /vscode/bin/linux-x64/2901c5ac6db8a986a5666c3af51ff804d05af0d4/out/bootstrap-fork --type=fileWatcher
root          57  0.2  0.8 1966712 69888 ?       Sl   09:01   0:00 dockerd --dns 168.63.129.16
@patelpayal8 ➜ /workspaces/Devops-Learning (main) $ 