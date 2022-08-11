# redmine
・virtualbox上で共有設定をしている環境で構築。Volume(bind)設定はHome下では設定できないため(Chmodで変更できない)共有下ではない/var/docker/redmineをbind指定している。設定に必要なDirは/home/redmine/data下にあるので適切なDirにPluginたテーマ情報をDLしコンテナを再起動することで利用できる。
・docker-compose up -d で起動。
・Dockerfileは特に変更は加えていない。(参考確認用)

■データベースの設定について　http://guide.redmine.jp/RedmineInstall/#sql-server

■plugins(/home/redmine/data/plugins)
git clone --depth 1 https://github.com/syagawa/redmine_absolute_datetime && \
git clone --depth 1 https://github.com/haru/redmine_wiki_extensions && \
git clone --depth 1 https://github.com/suer/redmine_japanese_help && \
git clone --depth 1 https://github.com/haru/redmine_theme_changer && \
git clone --depth 1 https://github.com/vividtone/redmine_gantt_with_date.git && \
git clone --depth 1 https://github.com/zh/redmine_importer.git && \
git clone --depth 1 https://github.com/two-pack/redmine_xlsx_format_issue_exporter.git &&\
git clone --depth 1 https://github.com/akiko-pusu/redmine_issue_templates.git

■テーマ(/home/redmine/data/themes)
git clone --depth 1 https://github.com/akabekobeko/redmine-theme-minimalflat2 && \
git clone --depth 1 https://github.com/themondays/Dwarf && \
git clone --depth 1 https://github.com/tsi/redmine-theme-flat && \
git clone --depth 1 https://github.com/hardpixel/minelab && \
git clone --depth 1 https://github.com/lqez/redmine-theme-basecamp-with-icon && \
git clone --depth 1 https://github.com/makotokw/redmine-theme-gitmike && \
git clone --depth 1 https://github.com/farend/redmine_theme_farend_basic && \
git clone --depth 1 https://github.com/farend/redmine_theme_farend_fancy && \
git clone --depth 1 https://github.com/Nitrino/flatly_light_redmine && \
git clone --depth 1 https://github.com/mrliptontea/PurpleMine2 && \
git clone --depth 1 https://github.com/Froiden/fedmine && \
git clone --depth 1 https://github.com/vsc55/redmine-theme && \
git clone --depth 1 https://github.com/FabriceSalvaire/redmine-improved-theme
