# TPE_THROAT_CUT_NEWS
Analysis of Taipei Throat Cutted Related News

_In Memory of Throat Cutted Yough Girl_

see [2015年臺北市文化國小隨機殺人事件](http://zh.wikipedia.org/wiki/2015年臺北市文化國小隨機殺人事件)

# 1. Data Collection #

News data was collected by UDN news, and can be downloaded at: [割喉案媒體報導多煽動？ 數據告訴你](http://p.udn.com.tw/upf/newmedia/2015_data/20150602_udnthroat/udnthroat/index.html "UDN")


# 2. Analysis Approach #
## Step 1 ##
Applying *Weighted Rich Degree Algorithm* over Pair-wised Mutual Informaion of each two adjoint words. 
![Weighted_Rich_Degree](http://blog.fychao.info/wp-content/uploads/2015/06/Weighted_Rich_Degree.jpg)

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>appledaily</th>
      <th>cna</th>
      <th>ctnews</th>
      <th>ettoday</th>
      <th>ltn</th>
      <th>udn</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0 </th>
      <td>  女童</td>
      <td>   校園</td>
      <td>  表示</td>
      <td>  女童</td>
      <td>  校園</td>
      <td>  校園</td>
    </tr>
    <tr>
      <th>1 </th>
      <td>  表示</td>
      <td>   表示</td>
      <td>  女童</td>
      <td>  表示</td>
      <td>  表示</td>
      <td>  表示</td>
    </tr>
    <tr>
      <th>2 </th>
      <td>  社會</td>
      <td>   學校</td>
      <td>  社會</td>
      <td>  社會</td>
      <td>  女童</td>
      <td>  女童</td>
    </tr>
    <tr>
      <th>3 </th>
      <td>  死刑</td>
      <td>   女童</td>
      <td>  死刑</td>
      <td>  死刑</td>
      <td>  學校</td>
      <td>  學校</td>
    </tr>
    <tr>
      <th>4 </th>
      <td>  校園</td>
      <td>   安全</td>
      <td>  發生</td>
      <td> 龔重安</td>
      <td>  加強</td>
      <td>  社會</td>
    </tr>
    <tr>
      <th>5 </th>
      <td>  學校</td>
      <td>   今天</td>
      <td>  台灣</td>
      <td>  沒有</td>
      <td>  社會</td>
      <td>  安全</td>
    </tr>
    <tr>
      <th>6 </th>
      <td>  警方</td>
      <td>   社會</td>
      <td>  校園</td>
      <td>  校園</td>
      <td>  龔嫌</td>
      <td>  沒有</td>
    </tr>
    <tr>
      <th>7 </th>
      <td>  沒有</td>
      <td>   加強</td>
      <td>  沒有</td>
      <td>  學校</td>
      <td>  安全</td>
      <td>  死刑</td>
    </tr>
    <tr>
      <th>8 </th>
      <td>  安全</td>
      <td>   進行</td>
      <td>  警方</td>
      <td>  臉書</td>
      <td>  死刑</td>
      <td>  加強</td>
    </tr>
    <tr>
      <th>9 </th>
      <td>  台灣</td>
      <td>   發生</td>
      <td>  我們</td>
      <td>  家屬</td>
      <td>  警方</td>
      <td>  警方</td>
    </tr>
    <tr>
      <th>10</th>
      <td>  發生</td>
      <td>   要求</td>
      <td>  希望</td>
      <td>  發生</td>
      <td>  民眾</td>
      <td>  今天</td>
    </tr>
    <tr>
      <th>11</th>
      <td>  龔嫌</td>
      <td>   巡邏</td>
      <td>  自己</td>
      <td>  指出</td>
      <td>  記者</td>
      <td>  發生</td>
    </tr>
    <tr>
      <th>12</th>
      <td>  我們</td>
      <td>   圍牆</td>
      <td>  編輯</td>
      <td>  自己</td>
      <td>  認為</td>
      <td>  家屬</td>
    </tr>
    <tr>
      <th>13</th>
      <td>  民眾</td>
      <td>   事件</td>
      <td>  認為</td>
      <td>  警方</td>
      <td>  臉書</td>
      <td>  廁所</td>
    </tr>
    <tr>
      <th>14</th>
      <td>  嫌犯</td>
      <td>   家屬</td>
      <td>  孩子</td>
      <td>  台灣</td>
      <td>  沒有</td>
      <td>  要求</td>
    </tr>
    <tr>
      <th>15</th>
      <td>  認為</td>
      <td>   沒有</td>
      <td>  開放</td>
      <td>  進行</td>
      <td>  今天</td>
      <td>  認為</td>
    </tr>
    <tr>
      <th>16</th>
      <td>  加強</td>
      <td>   協助</td>
      <td>  民眾</td>
      <td>  希望</td>
      <td>  指出</td>
      <td>  學生</td>
    </tr>
    <tr>
      <th>17</th>
      <td>  自己</td>
      <td>   喉案</td>
      <td> 龔重安</td>
      <td>  安全</td>
      <td>  發生</td>
      <td>  進行</td>
    </tr>
    <tr>
      <th>18</th>
      <td>  希望</td>
      <td>  台北市</td>
      <td>  是否</td>
      <td>  目前</td>
      <td>  台灣</td>
      <td>  指出</td>
    </tr>
    <tr>
      <th>19</th>
      <td>  報導</td>
      <td>   指出</td>
      <td>  發現</td>
      <td>  認為</td>
      <td>  嫌犯</td>
      <td>  問題</td>
    </tr>
    <tr>
      <th>20</th>
      <td>  學生</td>
      <td>   台北</td>
      <td>  安全</td>
      <td>  事件</td>
      <td>  問題</td>
      <td>  警察</td>
    </tr>
    <tr>
      <th>21</th>
      <td>  學童</td>
      <td>   維護</td>
      <td>  網友</td>
      <td>  我們</td>
      <td>  昨天</td>
      <td>  時間</td>
    </tr>
    <tr>
      <th>22</th>
      <td>  小妹</td>
      <td>  龔重安</td>
      <td>  國小</td>
      <td>  他們</td>
      <td>  學生</td>
      <td>  巡邏</td>
    </tr>
    <tr>
      <th>23</th>
      <td>  目前</td>
      <td>   希望</td>
      <td>  廢死</td>
      <td>  問題</td>
      <td>  目前</td>
      <td> 龔重安</td>
    </tr>
    <tr>
      <th>24</th>
      <td>  國小</td>
      <td>   警方</td>
      <td>  龔嫌</td>
      <td>  嫌犯</td>
      <td>  學童</td>
      <td>  學童</td>
    </tr>
    <tr>
      <th>25</th>
      <td>  廢死</td>
      <td>   學生</td>
      <td>  看到</td>
      <td>  感到</td>
      <td>  自己</td>
      <td>  民眾</td>
    </tr>
    <tr>
      <th>26</th>
      <td> 台北市</td>
      <td>   問題</td>
      <td> 民進黨</td>
      <td>  網友</td>
      <td>  進行</td>
      <td>  事件</td>
    </tr>
    <tr>
      <th>27</th>
      <td>  台北</td>
      <td>   警察</td>
      <td>  要求</td>
      <td>  下午</td>
      <td>  希望</td>
      <td>  校方</td>
    </tr>
    <tr>
      <th>28</th>
      <td>  警察</td>
      <td>  警察局</td>
      <td>  引發</td>
      <td>  要求</td>
      <td>  事件</td>
      <td>  協助</td>
    </tr>
    <tr>
      <th>29</th>
      <td>  今天</td>
      <td>   人員</td>
      <td>  家長</td>
      <td>  如何</td>
      <td>  我們</td>
      <td>  希望</td>
    </tr>
    <tr>
      <th>30</th>
      <td>  時間</td>
      <td>   上午</td>
      <td>  時間</td>
      <td>  龔嫌</td>
      <td> 龔重安</td>
      <td>  是否</td>
    </tr>
    <tr>
      <th>31</th>
      <td>  討論</td>
      <td>   搶救</td>
      <td>  工作</td>
      <td>  國小</td>
      <td>  要求</td>
      <td>  圍牆</td>
    </tr>
    <tr>
      <th>32</th>
      <td>  可能</td>
      <td>   死刑</td>
      <td>  什麼</td>
      <td>  晚間</td>
      <td>  報導</td>
      <td>  目前</td>
    </tr>
    <tr>
      <th>33</th>
      <td>  問題</td>
      <td>   學童</td>
      <td>  這個</td>
      <td>  民眾</td>
      <td>  網友</td>
      <td>  校安</td>
    </tr>
    <tr>
      <th>34</th>
      <td>  要求</td>
      <td> 今天上午</td>
      <td>  過去</td>
      <td>  報導</td>
      <td>  巡邏</td>
      <td>  昨天</td>
    </tr>
    <tr>
      <th>35</th>
      <td>  事件</td>
      <td>   是否</td>
      <td>  教育</td>
      <td>  搶救</td>
      <td>  國小</td>
      <td>  廢死</td>
    </tr>
    <tr>
      <th>36</th>
      <td>  老師</td>
      <td>   家長</td>
      <td>  今天</td>
      <td>  孩子</td>
      <td>  可能</td>
      <td>  家長</td>
    </tr>
    <tr>
      <th>37</th>
      <td> 龔重安</td>
      <td>   相關</td>
      <td>  民調</td>
      <td>  犯案</td>
      <td>  家長</td>
      <td>  檢討</td>
    </tr>
    <tr>
      <th>38</th>
      <td>  是否</td>
      <td>   校安</td>
      <td>  如何</td>
      <td>  協助</td>
      <td>  圍牆</td>
      <td>  兒童</td>
    </tr>
    <tr>
      <th>39</th>
      <td>  不能</td>
      <td>   教育</td>
      <td>  執行</td>
      <td>  廢死</td>
      <td>  喉案</td>
      <td>  工作</td>
    </tr>
    <tr>
      <th>40</th>
      <td>  文化</td>
      <td>   昨天</td>
      <td>  問題</td>
      <td>  記者</td>
      <td>  教育</td>
      <td>  自己</td>
    </tr>
    <tr>
      <th>41</th>
      <td>  家屬</td>
      <td>   認為</td>
      <td>  可能</td>
      <td> 小妹妹</td>
      <td>  廢死</td>
      <td> 警察局</td>
    </tr>
    <tr>
      <th>42</th>
      <td>  網友</td>
      <td>   校方</td>
      <td>  學生</td>
      <td>  什麼</td>
      <td>  台北</td>
      <td>  台灣</td>
    </tr>
    <tr>
      <th>43</th>
      <td>  進行</td>
      <td>   這個</td>
      <td>  犯案</td>
      <td>  家長</td>
      <td>  時間</td>
      <td>  無法</td>
    </tr>
    <tr>
      <th>44</th>
      <td>  現場</td>
      <td>  宋文舉</td>
      <td>  保全</td>
      <td>  相關</td>
      <td>  警局</td>
      <td>  狀況</td>
    </tr>
    <tr>
      <th>45</th>
      <td>  臉書</td>
      <td>   狀況</td>
      <td>  事件</td>
      <td> 台北市</td>
      <td>  分局</td>
      <td>  維護</td>
    </tr>
    <tr>
      <th>46</th>
      <td>  家長</td>
      <td>   包括</td>
      <td>  嫌犯</td>
      <td>  大家</td>
      <td> 教育局</td>
      <td>  人員</td>
    </tr>
    <tr>
      <th>47</th>
      <td>  這些</td>
      <td>   記者</td>
      <td>  社區</td>
      <td>  北投</td>
      <td>  開放</td>
      <td>  不能</td>
    </tr>
    <tr>
      <th>48</th>
      <td>  廁所</td>
      <td>   檢討</td>
      <td> 台北市</td>
      <td>  未來</td>
      <td>  人員</td>
      <td> 教育局</td>
    </tr>
    <tr>
      <th>49</th>
      <td>  緊急</td>
      <td>   在校</td>
      <td>  學校</td>
      <td>  是否</td>
      <td>  犯案</td>
      <td>  緊急</td>
    </tr>
    <tr>
      <th>50</th>
      <td>  龔男</td>
      <td>   弟弟</td>
      <td>  成為</td>
      <td>  學生</td>
      <td>  家屬</td>
      <td>  在校</td>
    </tr>
    <tr>
      <th>51</th>
      <td>  引發</td>
      <td>   未來</td>
      <td>  指出</td>
      <td>  接受</td>
      <td> 台北市</td>
      <td> 台北市</td>
    </tr>
    <tr>
      <th>52</th>
      <td>  喉案</td>
      <td>   廁所</td>
      <td>  立委</td>
      <td>  加強</td>
      <td>  孩子</td>
      <td>  喉案</td>
    </tr>
    <tr>
      <th>53</th>
      <td>  協助</td>
      <td>   周邊</td>
      <td>  震驚</td>
      <td>  引發</td>
      <td>  鄭捷</td>
      <td>  發現</td>
    </tr>
    <tr>
      <th>54</th>
      <td>  工作</td>
      <td>   不要</td>
      <td>  員警</td>
      <td>  這些</td>
      <td>  有人</td>
      <td>  社區</td>
    </tr>
    <tr>
      <th>55</th>
      <td>  發現</td>
      <td>   輔導</td>
      <td>  他們</td>
      <td>  輔導</td>
      <td>  引發</td>
      <td>  教育</td>
    </tr>
    <tr>
      <th>56</th>
      <td>  政府</td>
      <td>   主任</td>
      <td>  擔任</td>
      <td>  喉案</td>
      <td>  強調</td>
      <td>  孩子</td>
    </tr>
    <tr>
      <th>57</th>
      <td>  生命</td>
      <td>   目前</td>
      <td>  粉絲</td>
      <td>  政府</td>
      <td>  無法</td>
      <td>  包括</td>
    </tr>
    <tr>
      <th>58</th>
      <td>  不要</td>
      <td>   晚間</td>
      <td>  進行</td>
      <td>  醫師</td>
      <td> 警察局</td>
      <td>  上午</td>
    </tr>
    <tr>
      <th>59</th>
      <td>  應該</td>
      <td>   工作</td>
      <td>  犯下</td>
      <td>  台北</td>
      <td>  相關</td>
      <td>  各校</td>
    </tr>
    <tr>
      <th></th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
  </tbody>
</table>

## Step 2 ##
Applying LSA over news articles and using labeled 20-topics for ranking news channels. Manual labeled 20-topics are generated by LSA, and the top 10 labels are:

<table>
    <tr>
<td> 集合 1 (事件說明1) <td> 校園 安全 學校 警方 加強 柯文 死刑 分局 龔嫌 圍牆 女童 巡邏 龔重安 嫌犯 學童 維護 社會 北投 文化 </td></tr>
<td> 集合 2 (事件說明2)<td> 校園 安全 加強 學校 龔嫌 巡邏 維護 龔重安 死刑 女童 檢測 心跳 嫌犯 氣管 協助 士林 警察局 各級 周邊 
</td></tr><td> 集合 3 (死刑/廢死)<td> 死刑 廢死 廢除 台灣 心跳 總統 議題 龔嫌 氣管 警方 分局 網友 立委 蔡正元 柯文 支持 民進黨 臉書 士林
</td></tr><tr><td> 集合 4 (送醫)<td> 
龔嫌 士林 龔男 宋文舉 分局 氣管 移送 龔重安 心跳 闖入 外科 北榮 警方 搶救 羈押 弟弟 手術 斷裂 生命
</td></tr><tr><td> 集合 5 (家屬道歉)<td> 
弟弟 哥哥 道歉 死刑 出面 家屬 家人 士林 知道 廢死 柯文 父親 闖入 移送 什麼 廢除 檢署 總統 下跪
</td></tr><tr><td> 集合 6 (北市作為1)<td> 
柯文 專案 檢討 檢測 維護 哲說 邱豐光 各級 安全 圍牆 警局 教育局 相驗 弟弟 周邊 會議 小組 警察 議會 
</td></tr><tr><td> 集合 7 (死亡說明)<td> 
相驗 弟弟 翁偉倫 哥哥 小妹 檢察 士林 氣管 道歉 死刑 斷裂 檢署 小妹妹 遺體 圍牆 血管 眼淚 警方 闖入 
</td></tr><tr><td> 集合 8 (北市作為2)<td> 
圍牆 柯文 開放 朱立倫 相驗 郝龍斌 專案 廁所 社區 警察局 降低 弟弟 監視器 加強 翁偉倫 友善 政策 高度
</td></tr><tr><td> 集合 9 (犯嫌角度)<td>
弟弟 圍牆 龔男 哥哥 朱立倫 士林 羈押 道歉 闖入 郝龍斌 宋文舉 嫌犯 總統 逮獲 臉書 廁所 遭翻 吳克群
</td></tr><td> 集合 10(官員說)<td> 
輔導 總統 英文 廢除 蔡正元 宋文舉 民進黨 相驗 老師 吳克群 龔重安 弟弟 廢死 普世 馬英九 立委 朱立倫
</td></tr>
</table>



<table>
    <tr><td> <td> Rank 1<td> Rank 2	<td> Rank 3	<td> Rank 4	<td> Rank 5	<td> Rank 6 </td>
</tr><tr> <td>事件說明1<td>LTN	<td>UDN	<td>APPLEDAILY	<td>ETTODAY	<td>CNA	<td>CTNEWS
</tr><tr> <td>事件說明2<td>UDN	<td>LTN	<td>CNA	<td>APPLEDAILY	<td>ETTODAY	<td>CTNEWS
</tr><tr> <td>死刑/廢死<td>ETTODAY	<td>APPLEDAILY	<td>LTN	<td>CTNEWS	<td>UDN	<td>CNA
</tr><tr> <td>送醫<td>ETTODAY	<td>CNA	<td>LTN	<td>APPLEDAILY	<td>UDN	<td>CTNEWS
</tr><tr><td>家屬道歉<td>ETTODAY	<td>APPLEDAILY	<td>CTNEWS	<td>LTN	<td>CNA	<td>UDN
</tr><tr> <td>北市作為1<td>CNA	<td>UDN	<td>LTN	<td>APPLEDAILY	<td>ETTODAY	<td>CTNEWS
</tr><tr> <td>死亡說明<td>ETTODAY	<td>CNA	<td>APPLEDAILY	<td>LTN	<td>UDN	<td>CTNEWS
</tr><tr><td>北市作為2<td>UDN	<td>CNA	<td>LTN	<td>APPLEDAILY	<td>ETTODAY	<td>CTNEWS
</tr><tr><td>犯嫌角度<td>CNA	<td>ETTODAY	<td>LTN	<td>UDN	<td>APPLEDAILY	<td>CTNEWS
</tr><tr><td>官員說<td>ETTODAY	<td>CTNEWS	<td>APPLEDAILY	<td>LTN	<td>CNA	<td>UDN
</td></tr>
</table>

List of news channel (alphabetic):

* APPLEDAILY, [蘋果日報](http://www.appledaily.com.tw)
* CNA, [中央社即時新聞](http://www.cna.com.tw)
* CTNEWS, [中時電子報](http://www.chinatimes.com)
* ETTODAY,[東森新聞雲](http://www.ettoday.net)
* LTN, [自由時報電子報](http://www.ltn.com.tw)
* UDN, [聯合新聞網](http://udn.com) 

