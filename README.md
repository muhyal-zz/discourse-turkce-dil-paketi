# discourse-turkce-dil-paketi
Discourse için özel Türkçe dil paketidir (Resmi sürüm dil paketini kullanmak istemeyenler için.).

Kurulum için altta vermiş olduğum kodu `/var/discourse/containers/app.yml` dosyasına ekleyin.

```
hooks:
  after_code:
    - exec:
        cd: $home/plugins
        cmd:
          - mkdir -p plugins
          - git clone https://github.com/muhyal/discourse-turkce-dil-paketi.git
```
Daha sonra Discourse'u şu komut ile yeniden yapılandırın `/var/discourse/launcher rebuild app`
