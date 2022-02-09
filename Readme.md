เมื่อเขียน dockerfile ได้ตามต้องการแล้วต่อไปสั่ง build ด้วยคําสั่ง

docker build -t myimage .
-t blink คือการระบุชื่อและ tag ของ Docker Image ในตัวอย่างนี้ใช้ชื่อว่า blink

.  คือ path ของ dockerfile

จบขั้นตอนการสร้าง Image ถ้าต้องการที่จะลบ Docker Image ให้ใช้คําสั่ง

docker rmi image_name

image_name คือชื่อของ image ที่ต้องการลบ

Run Docker Image ที่สร้างขึ้น
ในหัวข้อนี้จะเป็นการ run Docker Image ที่เราสร้างไว้เมื่อกี้ มีขั้นตอนดังนี้ ใช้คําสั่ง

docker run -d -p 3000:3000 myimage
-d คือให้ run แบบ background
myimage คือ ชื่อของ Docker Image ที่ต้องการจะ run