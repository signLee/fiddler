# fiddler
fiddler use construction


���ã�(����ץȡhttps����)
tools--->options--->https--->��ѡcapture HTTPS CONNECTs������https���ӣ���decrypt HTTPS traffic������https��������ignore server certificate errors������https����

F12��ʼ��׽��Ĭ���Ǵ�״̬��
autoResponder����ַ���� ��Զ�̵�ַ��������·��  �����ڽ����ص�ַ�������Ե�ַ
enable rules��ѡ->unmatched requests passthrough����ƥ������ͨ������ѡ
add rule:
EG:�Ѱٶȵĵ�ַ���������ļ�
EXACT:https://www.baidu.com/  //���ʵ�ַ
C:\Users\sign\Desktop\test.txt   //���ش����ַ
save

composer���ط�������
type:POST
http://test.msjk95596.com/rest/personnel/svr/v0/recruitinfo/page
����Content-Type: application/json
request Body���������
{
	"pageNo": 0, 
	"pageSize": 10,
	"jobType": "", 
	"status": "online"
}
execute���ýӿ�
�鿴�ӿڷ�����Ϣ��
˫�����ӣ�Inspectors���ǹ��ڽӿڵĸ�����Ϣ���ײ��ǽӿڷ��صĸ�����Ϣ

�����������fiddler��������->�߼�->����->����firfox������ӵ�������--->ʹ��ϵͳ��������

filters������ָ����վ
EG:
����Ҫץȡhttps://www.xxxx.com/wxproduct/getProductLoanList������ӵ�����
Filter:
��ѡuse Filters
host��ѡ������������ (www��ͷ��Ϊ����)
����ѡ���������
��д��ַ ��www.xxxx.com
request header�ﹴѡshow only fi URL contains����д�ӿ�����wxproduct/getProductLoanList	
����fiddler��ֻ��ץhttps://www.xxxx.com/wxproduct/getProductLoanList������ӵ�������


fiddler�ϵ�ʹ�ã�F11  ������������ǰ�ϵ�������ϵ� rules-----automatic breakoptions ---before request  һ�����filterʹ��
�������---------break on response-----textview���Ƿ��ص����ݣ��޸ĺú��run to completion��ʵ�����޸ĺ�̨���ص�����

����Զ�̵��ԣ�����ץȡ�ֻ�����
tools----options------connections--allow remote computers to connect -----����flddler
�ֻ���PC������ͬһ����
�ֻ����ã�wifi----http����---����PC�˵�ip�Ͷ˿ں�-----����PC��ip��ַ�Ͷ˿ں�-------����֤�鰲װ---ͨ��-����-���ڱ���-----����֤��




