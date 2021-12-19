<!-- image build -->
docker build -t composer2.x:local .
<!-- create laravel project with user 1000 -->
docker run -u 1000:1000 --rm -it --name composer -v "$(pwd)/src:/var/www/html" composer2.x:local create-project --prefer-dist laravel/laravel .