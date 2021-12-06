# MirthWebCrawler

## Install Instructions 
Download and install Mirth Connect from the NextGen Website:

https://www.nextgen.com/products-and-services/mirth-connect-downloads

Download and install MySQL along with MySQL Workbench: 

https://dev.mysql.com/downloads/

Luanch MySQL Workbench, run the MySQL commands found in the SQL.txt file.  This will create a Mirth user along with the required tables and stored procs to run the two channels.

Luanch Mirth connect and login useing the default username and password: _admin/admin_

Once within the Mirth Application user **Mirth Connect** click **Channels**. This will take to take you to the channels view.  A new tab will appear **Group Tasks** Click **Import Group** and Import **Web Crawler.xml** which you have saves to your desktop somewhere.  When Asked to Import addtional libraries click yes and select all of the Hikari DB tables listed.  Select **Import** and now a new group called ** Web Crawler** should exists.  Under this group should be two channels **Parse Words** and **Scrap Words** 

The channels utlize the **Jsoup** library so it will need to be added as a useable library.  To do this download Jsoup from the following source: 

https://jsoup.org/packages/jsoup-1.14.3.jar

Save this file in the Mirth custom-lib drectory located at `C:\Program Files\Mirth Connect\custom-lib`

Back within the Mirth Application navigate to the **Settings** under the **Mirth Connect** table.  At the table select **Resources** and on the left a new tab **Resouce Tasks** should appear.  Select **Reload Resources** Sleect **Yes** and you should now see the Jsoup .jar under **Loaded Libraries**

To use the Scraper navigate back to the **Channels** table within the Mirth application.  Right click on each of the channels and select **Deploy Channel** for each.  With will start the the scrapper and word count to collect data.  

*Note each channel is set to run only once a minute if you wish to change this then uder the srouce for each channel change the Interval as desired and redeploy for changes to take effect. 



 


