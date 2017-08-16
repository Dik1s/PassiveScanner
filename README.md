## ����
����һ������Mitmproxy��Arachni�ı���ʽɨ������
* arachni
* celery
* mitmproxy

![��������ͼ.png](https://github.com/jjf012/PassiveScanner/raw/master/images/process.png)

����Ϊ���ܹ���`celery`������windows���棬��ѡ��İ汾��3.1.25��
redis��Ϊcelery��broker�������������롣
ͨ��`celery -A scan worker --loglevel=info`����worker��
`proxy.py`��Ĭ�϶˿���8080��

![mysql.png](https://github.com/jjf012/PassiveScanner/raw/master/images/mysql.png)

**����**

2017/8/16
����vuln.sql���ݿ�ṹ�ļ�
����parser����һЩ����Ĵ���
����׺�ж��Ƶ�proxy��������
���Ӽ򵥵�ȥ�ع��ܣ���һ����Ȼ��hash����

�ο�����
* [����Arachni�����ں�ɨ��ƽ̨](http://bobao.360.cn/learning/detail/3533.html)
* [wyproxy](https://github.com/ring04h/wyproxy)
* [Arachni](https://github.com/Arachni/arachni/wiki/REST-API)
* [arachni-python-client](https://github.com/yukito/arachni-python-client)

## English
This is a passive scanner based on Mitmproxy and Arachni.
* Arachni
* Celery
* Mitmproxy

Which in order to be able to `celery` run on windows, I chose the version is 3.1.25.
Redis as celery broker and set the password.
Start worker with `celery -A scan worker - loglevel = info`.
The default port for `proxy.py` is 8080.

**update**

2017/8/16
add vuln.sql
Adjust the parser inside some of the redundant code
Move the suffix judgment to the proxy code
Increase url, normalized and then hash calculation

Reference link
* [Based on Arachni build black box scanning platform](http://bobao.360.cn/learning/detail/3533.html)
* [Wyproxy](https://github.com/ring04h/wyproxy)
* [Arachni](https://github.com/Arachni/arachni/wiki/REST-API)
* [arachni-python-client](https://github.com/yukito/arachni-python-client)