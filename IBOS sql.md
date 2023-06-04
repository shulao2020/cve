SQL injection exists in ibos office OA

Official website address:http://www.ibos.com.cn/

verison :v4.5.5

Route: r=dashboard/approval/del

![WPS图片(1)](https://github.com/shulao2020/cve/assets/135507126/72285f04-fdab-473b-abdc-05ef5e561377)

![WPS图片(2)](https://github.com/shulao2020/cve/assets/135507126/adc3a202-7616-4dd4-a3bd-a818fabc7de6)

Follow through with this method by calling model()->deleteApproval() through the actionDel() method

![WPS图片(3)](https://github.com/shulao2020/cve/assets/135507126/8395cb63-7770-4daf-bbcb-14dd9c7d2774)

The createCommand()->update() method is called regardless of the branch in the method

![WPS图片(4)](https://github.com/shulao2020/cve/assets/135507126/26842edc-85e4-48fd-9f3b-475e28b18519)


The SQL statement is executed with execute() in this method

![WPS图片(5)](https://github.com/shulao2020/cve/assets/135507126/c75abbdf-aba8-4200-87aa-d6d0600ccb1f)
