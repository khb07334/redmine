# redmine
・virtualbox上で共有設定をしているため、Volume(bind)設定はHome下では設定できないため(Chmodで変更できない)
  共有下ではない/var/docker/redmineをbind指定している。設定に必要なDirは/home/redmine/data下にあるので
  適切なDirにPluginたテーマ情報をDLしコンテナを再起動することで利用できる。
・docker-compose up -d で起動。
・Dockerfileは特に変更は加えていない。(参考確認用)
