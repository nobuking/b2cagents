# 2018/9月時点で動作確認済みのバージョン
FROM fluent/fluentd:v1.2

# below RUN includes plugin as examples elasticsearch is not required
# you may customize including plugins as you wish

RUN apk add --update --virtual .build-deps \
        sudo build-base ruby-dev \
 && sudo fluent-gem install \
        fluent-plugin-elasticsearch fluent-plugin-suppress fluent-plugin-record-modifier\
 && sudo gem sources --clear-all \
 && apk del .build-deps \
 && rm -rf /var/cache/apk/* \
           /home/fluent/.gem/ruby/2.4.0/cache/*.gem
