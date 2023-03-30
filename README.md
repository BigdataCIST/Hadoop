# Hadoop

### Mục lục 
[Cài đặt và cấu hình Hadoop Cluster](#install_hadoop_cluster)
* [Giới thiệu chung](#overview)
* [Cài đặt](#install)

<a name="install_hadoop_cluster"></a>
## Cài đặt và cấu hình Hadoop Cluster
**Bài toán đặt ra:**
* Dữ liệu luôn tăng và phần cứng thì có giới hạn nên không thể lưu trữ hết lượng dữ liệu khổng lồ cũng như xử lý tính toán chúng trên một máy tính đơn lẻ. Do đó ta sẽ lưu trữ và xử lý dữ liệu đó trên nhiều máy đơn lẻ  

$\rightarrow$ Cần một hệ thống quản lý lưu trữ và xử lý dữ liệu lớn được phân tán trên các các máy tính

$\rightarrow$ Giải pháp: Hadoop (nó là cái gì có ăn được không? Đọc tiếp sẽ rõ 😁)
<a name="overview"></a>
### Giới thiệu chung 
[Hadoop](https://hadoop.apache.org/) là một dự án Apache mã nguồn mở cho phép lưu trữ và tạo các ứng dụng xử lý song song trên các tập dữ liệu lớn, được phân phối trên các node (mỗi node là một máy tính) được kết nối mạng.

[Hadoop](https://hadoop.apache.org/) gồm các module sau:
* Hadoop Common: là các thư viện, tiện ích được viết bằng Java 
* Hadoop Distributed File System (HDFS): cung cấp giải pháp lưu trữ phân tán cũng như là dự phòng dữ liệu, được thiết kế để chạy trên một cụm gồm nhiều node (mỗi node là một máy tính).
* Hadoop YARN: giúp lập lịch thực hiện các tác vụ xử lý dữ liệu trên tất cả các nodes.
* Hadoop MapReduce: là mô hình lập trình song song để xử lý dữ liệu lớn trên một cụm gồm nhiều node.

**Kiến trúc Hadoop Cluster**

Kiến trúc master/slave (chủ/tớ), gồm 2 loại node chính:
* **Master node:** lưu giữ thông tin về hệ thống file phân tán (Distributed File System - DFS), ngoài ra còn có nhiệm vụ lên kế hoạch phân bổ tài nguyên. Trong phần hướng dẫn cài đặt dưới đây, master node có 2 nhiệm vụ chính:
    * Name node: quản lý DFS, nắm bắt thông tin block dữ liệu nào nằm ở đâu trong cluster 
    * ResourceManager: quản lý các job của YARN và các lý các job được xếp lịch chạy trên các slave node.
* **Slave/worker nodes:** lưu dữ liệu thực và cung cấp sức mạnh phần cứng để chạy các job. Trong phần này, slave node có nhiệm vụ:
    * Datanode: quản lý các block dữ liệu về mặt vật lý.
    * Nodemanager: quản lý thực hiện các task trên node.  
 
<a name="install"></a>
### [Cài đặt](https://123host.vn/tailieu/kb/vps/cai-dat-va-cau-hinh-hadoop-cluster.html)
