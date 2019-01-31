使用DBeaver访问Kerberos环境下配置impala（Mac版本）
==================================================

1.  要编写清单，只需点击此处并开始键入。

    点击“dbeaver-ce-5.3.3-macos.dmg”安装，将DBeaver图标拖入到右边的Application的文件夹里

    ![](media/2feb566c5fa5f4ec52aa26218b465a6a.png)

2.  从访达进入应用程序，找到DBeaver，右键点击选择“显示包内容”。

    ![](media/9f9888fab415e5fa0f8494e5232f0539.png)

3.  将“dbeaver.ini”，“krb5.conf”两个文件放到/Applications/DBeaver.app/Contents/Eclipse

    ![](media/9183c361d9a165c3c651390a0ea9ca9b.png)

4.  从访达进入应用程序，找到实用工具里的“Ticket Viewer”，打开

    ![](media/46098f9b74406b237e8e941a65ce4a41.png)

5.  点击“添加身份”，输入身份 <finance/remote@SGMW.COM>，和密码

    ![](media/2ffd0f227338679778e1bb8d649da25c.png)

    ![](media/c66ea4aea0f9840273af81c388111cd0.png)

6.  从访达进入应用程序，找到DBeaver，打开

    ![](media/2c3ee1ba1a459168ec4a6483a6ebcbda.png)

7.  点“数据库”、“创建新连接”、“Hadoop/Big Data”，“选Cloudera Impala”，点下一步

    ![](media/3498dcb52e4148f171651cd911c04a99.png)

8.  点“编辑驱动设置”填入JDBC URL：

    jdbc:impala://10.1.126.235:21050/dm_finance;AuthMech=1;KrbHostFQDN=cnwulcdhnode01;KrbServiceName=impala;

    ![](media/cd6ebff91be4b5459212a427ec4a537b.png)

    ![](media/4f77cd5b2f5545c0bc0b675b6b4322fd.png)

9.  在库的位置，点“添加文件”，把“ImpalaJDBC41.jar”添加进去，点“找到类”，点确定

    ![](media/986fb86e39fcc7d7977b6d2fcf6c318a.png)

10. 点“测试链接(T)…”

    ![](media/e3a04b55a94637bc419fd50b53debed4.png)
