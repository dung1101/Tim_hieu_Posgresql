## 1) Installation

```
sudo apt update
sudo apt install postgresql postgresql-contrib
```

## 2) Architectural Fundamentals

PostgresSQL uses a client/server model. A PostgreSQL session consists of the following cooperating processes (programs):

- A server process, which manages the database files, accepts connections to the database from client applications, and performs database actions on behalf of the clients. The database server program is called postgres.

- The user's client(frontend) application that wants to perform database operations. Client applications can be very diverse in nature: a client could be a text-oriented tool, a graphical application, a web server that accesses the database to display web pages, or a specialized database maintenance tool. Some client applications are supplied with the PostgreSQL distribution; most are developed by users.

As is typical of client/server applications, the client and the server can be on different hosts. In that case they communicate over a TCP/IP network connection.

The PostgreSQL server can handle multiple concurrent connections from clients. To archieve this it starts ("forks") a new process for each connection. From that point on, the client and the new server process communicate without intervention by the original postgres process. Thus, the master server process always running, waiting for client connections, whereas client and associated server processes come and go.

## 1) Cài đặt

```
sudo apt update
sudo apt install postgresql postgresql-contrib
```

## 2) Kiến trúc cơ bản
PostgresSQL sử dụng mô hình client/server. Một phiên PostgreSQL bao gồm các tiến trình sau:

- Tiến trình server sẽ quản lý file cơ sở dữ liệu, chấp nhận các kêt nối đến db từ client application và thực hiện các hành động từ client. Database server program gọi là postgres.

- client muốn tương tác tới database. Client có thể là 1 text-oriented tool, 1 ứng dụng đồ họa, 1 web server ... Một vài client được cung cấp bởi PosgreSQL còn lại hầu hết phát triển bởi người dùng.

Như một đặc trưng của ứng dụng client/server, client và server có thể không cùng nằm trên host. Trong trường hợp đó chúng giao tiếp qua giao thức TCP/IP.

PostgreSQL server có thể xử lý nhiều kết nối đồng thời từ client. Để lamd được điều đó nó tạo ra một tiến trình mới cho mỗi kết nối. Từ đó các client và tiến trình mới khởi tạo sẽ giao tiếp mà ko can thiệp vào tiến trình chính postgres. Như vây, tiến trình server luôn luôn chạy, chờ đợi kết nối từ client, trong khi các lient và tiến trình tương ứng đến và đi.
