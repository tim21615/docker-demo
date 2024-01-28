### docker-demo:
1. pom檔 設置 `<finalName> docker-demo </finalName>` (確保產出的 jar檔名稱即為 docker-demo.jar)
2. `maven clean` (清空 target資料夾，過去曾打包該專案的 jar檔都會消失，詳細說明見 notion.)
3. `maven install` => 打包出(產出)jar檔 (在 target 資料夾)
4. 接下來只要執行 `java -jar docker-demo.jar` 即可以執行，但是這邊我們想要把執行指令包成 image，因此見 5.
5. 產出 Dockerfile: FROM的jdk 必須跟 專案的java版本一致
6. `docker build -t docker-demo .`，並且將產出的 image 推到 Dockerhub
7. 完成，可以透過 `docker pull` / `docker run` 將專案run起來 !
