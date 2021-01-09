<script text/javascript>
if(msg.indexOf("급식") !=-1 ) {
    var today = Math.floor(Math.random()*30)+1;
    var u = org.jsoup.Jsoup.connect("https://m.search.naver.com/search.naver?sm=tab_hty.top&where=m&query=영동고급식%22).get()
    var day = u.select("div.menu_info").eq(today).text().split("]")[0]
    var info = u.select("div.menu_info").eq(today).text().replace(/ /g,"\n").split("]")[1]
    replier.reply(day+"]\n"+info)
  }
<script/>
