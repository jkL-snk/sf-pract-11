# sf-pract-11

Скрипт Terraform для создания двух VM и скрипты для создания master и worker-нод Kubernetes с помощью kubectl.

Требования: Git, Terraform, аккаунт в Yandex Cloud, OAUTH-токен от аккаунта.

В файле meta.yml требуется изменить имя пользователя и публичный ключ на ваши. В файле variables.tf указать ваши идентификаторы облака и папки в облаке.

Порядок установки:

git clone https://github.com/jkL-snk/sf-pract-11.git

cd ./sf-pract-11

terraform apply

Потребуется ввести значение OAUTH-токена.
