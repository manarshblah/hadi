# استخدام صورة Nginx خفيفة وسريعة
FROM nginx:alpine

# نسخ كافة ملفات المشروع (index.html والمجلدات مثل images) إلى المجلد المخصص في Nginx
COPY . /usr/share/nginx/html

# كشف المنفذ 80
EXPOSE 80

# تشغيل Nginx في المقدمة
CMD ["nginx", "-g", "daemon off;"]