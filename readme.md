# DJango

## ベースイメージ作成
cd base
docker build -t django .

## Power shell で linux的なpwd
function pwd_as_linux {
  "/$((pwd).Drive.Name.ToLowerInvariant())/$((pwd).Path.Replace('\', '/').Substring(3))"
}

docker run --rm -v "$(pwd_as_linux)/src:/opt/apps" django django-admin startproject sanshin .

docker volume create --name sanshin_data

docker-compose up -d db

