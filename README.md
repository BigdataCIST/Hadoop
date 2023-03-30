# Hadoop

### Mục lục 
[Cài đặt và triển khai Hadoop single node](#install_single_node_hadoop)
  * [Điều kiện trước khi cài đặt](#prerequisites)
  * [Thiết lập user cho Hadoop](#user_setting)
  * [Download và Cài đặt Hadoop trên Ubuntu](#download_install_hadoop)
  * [Cấu hình và triển khai Hadoop Single Node (Pseudo-Distributed Mode)](#pseudo_distributed_mode)
  * [Cài đặt và cấu hình Hadoop Cluster](#install_hadoop_cluster)

<a name = "install_single_node_hadoop"></a>
## Cài đặt và triển khai Hadoop single node

<a name="prerequisites"></a>
### Điều kiện trước khi cài đặt

* **Cài đặt jdk:**

```
sudo apt-get install openjdk-11-jdk -y
```
* **Cài SSH và SSH Server**:
```
sudo apt-get install openssh-server openssh-client -y
```
<a name="user_setting"></a>
### Thiết lập user cho Hadoop

* **Tạo cặp khóa SSH và xác định vị trí sẽ được lưu trữ :**
```
ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
```
* **Sử dụng lệnh *cat* để lưu *public key* vào *authorized_keys* trong thư mục của SSH:**
```
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```
* **Phân quyền cho người dùng với lệnh *chmod* :**
```
chmod 0600 ~/.ssh/authorized_keys
```
* **Xác minh mọi thứ được thiết lập chính xác bằng cách ssh đến localhost:**
```
ssh localhost
```
<a name="download_install_hadoop"></a>
### Download và Cài đặt Hadoop trên Ubuntu
Tải về một phiên bản Hadoop trên trang phân phối chính thức của Hadoop tại : https://hadoop.apache.org/releases.html

![download_hadoop](https://user-images.githubusercontent.com/103992475/165662924-584e1e6d-789e-43ec-b4f0-93255002f77e.png)

Ấn vào ***binary*** trong ***binary download***

![link_download](https://user-images.githubusercontent.com/103992475/165663285-f64aacae-eead-4611-b480-4f2809b45155.png)

Click vào link đầu tiên để tải về máy tính

Bây giờ để file nén vừa tải về vào bất kì chỗ nào và giải nén nó ra bằng lệnh :
```
tar xvzf hadoop-3.2.3.tar.gz
```
<a name="pseudo_distributed_mode"></a>
### Cấu hình và triển khai Hadoop Single Node (Pseudo-Distributed Mode)

<a name="install_hadoop_cluster"></a>
## [Cài đặt và cấu hình Hadoop Cluster](https://123host.vn/tailieu/kb/vps/cai-dat-va-cau-hinh-hadoop-cluster.html)
