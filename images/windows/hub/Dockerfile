ARG baseImage="unityci/base:windows-latest"

FROM $baseImage

# Install unity hub
RUN powershell -Command Set-ExecutionPolicy Bypass -Scope Process -Force; \
  [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; \
  Invoke-WebRequest -Uri https://public-cdn.cloud.unitychina.cn/hub/prod/UnityHubSetup.exe -OutFile UnityHubSetup.exe; \
  Start-Process UnityHubSetup.exe -ArgumentList '/S' -Wait; \
  Remove-Item UnityHubSetup.exe
