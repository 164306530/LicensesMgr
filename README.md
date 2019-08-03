# LicensesMgr

卸载Token里的无用证书

![image](https://github.com/laomms/LicensesMgr/blob/master/1.png)


获取系统已安装密钥的证书列表。
函数:GetLicenseList(ItemList),证书列表返回到list of string.
使用说明(.net4.6):


vb.net:
        Dim ItemList As New List(Of String)
        Dim func As New LicenseManage.GetLicense
        Dim flags = func.GetLicenseList(ItemList)
        Do
            If flags <> 0 Then
                Exit Do
            End If
            Application.DoEvents()
        Loop
        Debug.Print(String.Join("*", ItemList))

c#

        List<string> ItemList = new List<string>();
        LicenseManage.GetLicense func = new LicenseManage.GetLicense();
            int flags = func.GetLicenseList(ref ItemList);
            do
            {
              Application.DoEvents();
            } while (flags == 0);
            Console.WriteLine(String.Join("*",ItemList));

