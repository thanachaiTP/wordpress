# Wordpress

## 1. ติดตั้ง Wordpress
```
git clone https://github.com/thanachaiTP/wordpress.git -b wp-fpm
cd wordpress
cp env.example .env
docker-compose up -d
```

## 2. เพิ่ม config redis cache ที่ html/wp-config.php
```
define( 'WP_CACHE_KEY_SALT', 'w_' );
define(' WP_REDIS_SELECTIVE_FLUSH', true);
define( 'WP_REDIS_HOST', 'redis' );
define( 'WP_REDIS_DATABASE', 1 );
define( 'WP_REDIS_PORT', 6379 );
```

## 3. ติดตั้ง Plugin redis object cache
ให้ login เข้าหลังบ้านของ wordpress แล้วติดต้ง plugin ชื่อ redis object cache ติดตั้งเสร็จให้เปิดใช้งานใช้ จากนั้นเข้าไปที่ เมนู ตั้งค่า -> redis กดปุ่ม Enable
