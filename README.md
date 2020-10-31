# ansible_samples

English First, Japanese Second.

# Prerequisites

- The environment construction of Ansible has been completed _ The following is the installation guide of the official document.
- Basically, complete the environment construction with pyenv and pipenv and use python3.7 or higher. It is recommended to install ansible with pipenv.
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
- For resource deployment, LINUX Distribution is adopted so that Ansible can connect to the corresponding server with SSH.

# Environment

- Define the connection to the server where you want to execute the processing by Ansible in .ssh / config.
- Specific examples are as follows

`` ```
Host sample_host
    HostName host_accesible_ip_address
    User ubuntu
    IdentityFile ~ / .ssh / sample.pem
    Port 22
    TCPKeepAlive yes
    IdentitiesOnly yes
`` ```

# Execution method

- cd sample
- ansible-playbook -v -i inventories / develop webservers.yml

# Description of each folder

- sample
  - Folders that follow Ansible best practices

# 前提条件

- Ansibleの環境構築を完了していること_以下は公式ドキュメントのInstallation Guide。
- 基本的に、pyenv, pipenvでの環境構築を完了してpython3.7以上を利用。pipenvでansibleをインストールすることを推奨する。
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
- 資源の展開は、SSHでAnsibleによる該当サーバへの接続ができるよう、LINUX Distributionを採用する。

# 環境構築

- .ssh/configに、Ansibleによる処理を実行したいサーバーへの接続を定義する。
	- 具体例は以下

```
Host sample_host
    HostName host_accesible_ip_address
    User ubuntu
    IdentityFile ~/.ssh/sample.pem
    Port 22
    TCPKeepAlive yes
    IdentitiesOnly yes
```

# 実行方法

- cd sample
- ansible-playbook -v -i inventories/develop webservers.yml

# 各フォルダの説明

- sample
  - Ansibleのベストプラクティスに従ったフォルダ

