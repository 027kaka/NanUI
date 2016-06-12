# NanUI
### ǰ��
NanUI��һ������ChromiumFX��Դ��Ŀ��.Net Winform����⣬ChromiumFX��Chromium Embedded Framework��.Netʵ�֡�������֪��Chromium Embedded Framework (CEF)���� Marshall Greenblatt ��2008�괴��Ŀ�Դ��Ŀ�������ڻ���Google Chromium��Ŀ����һ��Web�ؼ������Խ�Chrome������Ĺ��ܣ�ҳ����Ⱦ��JS ִ�У�Ƕ�뵽����Ӧ�ó���Ŀ�ܡ�CEF ��ΪǶ��ʽ�����������ʺϵ�Ӧ�ó���Ӧ����Htmlҳ����Ⱦ�����Ժܶ���򶼻���CEF��ΪӦ�ó����ṩ HTML ҳ����Ⱦ�Ĺ��ܣ����е��ʼǣ�΢��Windows�ͻ��ˣ����������֣�Evernote��GitHub Window Client��Q+��Adobe Brackets �ȡ�

�ڴ�֮ǰCEFӦ�ô��ʹ��C++�����п���������.Net��Ŀ��.Net����ԭ��˵ֻ������÷ֹ�ʡ�����ChromiumFX��Ŀ�ĵ�����.Net��Ŀ�����ܹ���CEF��һ�����ܽӴ�����ChromiumFX��Ŀ��Ҫע������������ĵ�ʵ�֣���Winform���濪������̫�����á��ڴ˱����£�NanUI����������

NanUI�����˴�ͳ��Winform������Ʒ�ʽ��ͨ��NanUI���ܹ�ʹ��Html5��CSS3��javascript���������Winform���档�������Ϥ����bootstrap��jQuery��WinJS�ȸ���CSS��JS��Ļ������ܹ�����ϲ�û�ͻ�Ҫ����Ƴ�����Ư����Winform���档���ԣ�ʹ��NanUI�����Winform������潫�����޿��ܡ�

![NanUI](http://images2015.cnblogs.com/blog/352785/201605/352785-20160518180435701-1461536015.png)

### Ը��
NanUI�ڷ�����һ��Ԥ�����ʱ����֧�ֽ�CEF�ĸ���֧���ļ������ڳ���Ŀ¼����ģ����Ǿ����ܳ�ʱ���˼�������°汾��NanUI���޳��˶Դ���ܵ�֧�֡�CEF����֧���ļ�����Ҫ�����õ���%APPDATA%\Net Dimension Studio\NanUI�����档

Ϊ����Ҫ����������Ϊ��ϣ��NanUI�ܹ���ǿ�ķ�չ���г�һ�պܶ�.Net��������NanUI���������棬��ô���ʱ��NanUI��CEF����֧���ļ�����ͬ.Net Frameworkһ����ϵͳͬ�ڡ�û���˻����⼸ʮ�ϰ��׵�.Net Framework����Ϊ����ϵͳͬ�ڣ����е�.Net���򶼵����������ǹ���ģ�û����Ը���Լ������������ʱ����.Net Framework�ߡ�

���ԣ���ϣ��NanUI CEF Runtime����ôһ���ܹ����ܶ�.Net������ʹ�á�


### ��������
�����ϲ��NanUI��Ŀ������Բ��뵽NanUI�Ŀ�����������Ȼ��Ҳ���Ը�ֱ���˵���֧���ҵĹ�����ʹ��֧������΢��ɨ�������ά�����Һ�һ�������ڵĿ��ȡ�

![֧����](http://images2015.cnblogs.com/blog/352785/201606/352785-20160608004055668-1675779685.png)

֧����ɨ�����ά��������߱�����

![΢��֧��](http://images2015.cnblogs.com/blog/352785/201606/352785-20160612234514761-199610391.jpg)

΢��ɨһɨ�����ά��������߱�����


QQȺ��
241088256

### �汾״̬
NanUI�汾
> 0.3.2 alphaԤ��

֧�ֵĲ���ϵͳ
> Windows XP�����ϰ汾

��С֧�� .NET �汾
> .NET Framework 4.0 Client Profile

��ǰCEF�汾
> CEF 3.2623.1401 Chromium 49.0.2623.10

### ���ʹ��
**����NanUI��**

NanUIʹ�÷ǳ��򵥡�����Ŀ��ֻ�����á�NetDimension.NanUI.dll��һ���⼴�ɡ��������û�м�⵽CEF���п⣬NanUI���ṩ���ص�ַ�����Զ�������Ӧ��֧���ļ���

**��ʼ��CEF����**

��Main������
```C#
static class Program
{
  /// <summary>
  /// Ӧ�ó��������ڵ㡣
  /// </summary>
  [STAThread]
  static void Main()
  {
    Application.EnableVisualStyles();
    Application.SetCompatibleTextRenderingDefault(false);

    HtmlUILauncher.EnableFlashSupport = true;	//����Flash֧��

    if (HtmlUILauncher.InitializeChromium())	//��ʼ��CEF����
    {
      //����������
      Application.Run(new MainFrame());
    }
  }
}
```

**����Html**

��ʼ����ɺ��ڴ����м̳�HtmlUIForm�࣬��������ҳ��ַ�������ҳ��ļ��ء�����ʹ�ñ�����Դ��Զ����ַ��NanUI���ṩ�˶�Ƕ��ʽ��Դ��֧�֣�������ο�Wiki�е����ʾ����
```C#
public class MainFrame : HtmlUIForm
{
	public MainFrame()
		: base("<ҳ���ַ>")
	{
		InitializeComponent();
		//... ���ֳ�ʼ������
	}
}

```

ֻ�����ϼ򵥵�������������˶�NanUI�ļ��ء�����������ƵĹ����ͽ��������ɣ�

����ʾ���У�����ϸչʾNanUI��ʹ�÷�������Ȼ��Ҳ����ͨ��WIKI���˽������Ϣ��

### ��ʾ��Ŀ
**CodeEditor**

NanUI.Demo.CodeEditor
NanUI.Demo.CodeEditor.Resources

����Ŀʹ��ǿ���JS��ĿCodeMirror�����Bootstrap����н��沼�֣�ʵ����һ���򵥵Ĵ���༭�����ܡ�

**Welcome**

NanUI.Demo.Welcome

����Ŀʹ��jQuery��Bootstrap�������棬��Ҫ��ʾ��NanUI��HTML5��CSS3��Flash��WebGL�ȼ�����֧�̶ֳȡ�

### CEF���п�����
| ˵��           | ��С  | ˵��  | ����                                                           |
| -------------- |------:|:-----:|:-------------------------------------------------------------:|
| ������װ��      | 73.0M | �Ƽ�  | [����](http://www.bolepa.com/NanUI/NanUIPackages/all.exe)             |
| ��Դ�ļ�        | 3.53M | ��Ҫ  | [����](http://www.bolepa.com/NanUI/NanUIPackages/resources.exe)       |
| 32λCEF���п�   | 24.4M |      | [����](http://www.bolepa.com/NanUI/NanUIPackages/x86/cef_x86.exe.exe)  |
| 32λFlash֧�ֿ� | 7.46M |      | [����](http://www.bolepa.com/NanUI/NanUIPackages/x86/flash_x86.exe)    |
| 64λCEF���п�   | 29.2M |      | [����](http://www.bolepa.com/NanUI/NanUIPackages/x64/cef_x64.exe.exe)  |
| 64λFlash֧�ֿ� | 10.2M |      | [����](http://www.bolepa.com/NanUI/NanUIPackages/x64/flash_x64.exe)    |

### �ο�
���ޣ���������д��Ҫ��д�ÿ죬�ǵô����Ҽ������ȣ���