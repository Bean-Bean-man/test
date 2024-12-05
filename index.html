import requests
import streamlit as st

def getAllBookstore():
    url = 'https://cloud.culture.tw/frontsite/trans/emapOpenDataAction.do?method=exportEmapJson&typeId=M' # 在這裡輸入目標 url
    headers = {"accept": "application/json"}
    response = requests.get(url, headers=headers)
    res = response.json()
    return res

def getCountyOption(items):
    # 創建一個空的 List 並命名為 optionList
    optionlist = []
    for item in items:
        # 把 cityname 欄位中的縣市名稱擷取出來 並指定給變數 name
        # hint: 想辦法處理 item['cityName'] 的內容
        name=item['cityName'][0:3]

        if name not in optionlist:
            optionlist.append(name)

        # 如果 name 不在 optionList 之中，便把它放入 optionList
        # hint: 使用 if-else 來進行判斷 / 用 append 把東西放入 optionList
    return optionlist

def getSpecificBookstore(items, county):
    specificBookstoreList = []
    for item in items:
        name = item['cityName']
        if county not in name:
            continue
        else:
            specificBookstoreList.append(item)
    return specificBookstoreList
	# 如果 name 不是我們選取的 county 則跳過
	# hint: 用 if-else 判斷並用 continue 跳過
    return specificBookstoreList

def getBookstoreInfo(items):
    expanderList = []
    for item in items:
        expander = st.expander(item['name'])
        expander.image(item['representImage'])
        expander.metric('hitRate', item['hitRate'])
        expander.subheader('Introduction')
        # 用 expander.write 呈現書店的 Introduction
        expander.write(item['intro'])
        expander.subheader('Address')
        # 用 expander.write 呈現書店的 Address
        expander.write(item['address'])
        expander.subheader('Open Time')
        # 用 expander.write 呈現書店的 Open Time
        expander.write(item['openTime'])
        expander.subheader('Email')
        # 用 expander.write 呈現書店的 Email
        expander.write(item['email'])
        expanderList.append(expander)
        # 將該 expander 放到 expanderList 中
    return expanderList

def app():
    bookstorelist = getAllBookstore()
	# 呼叫 getCountyOption 並將回傳值賦值給變數 countyOption
    countyOption=getCountyOption(bookstorelist)
    st.header('特色書店地圖')
    st.metric('Total bookstore', len(bookstorelist))
    county = st.selectbox('請選擇縣市', countyOption)  # 將['A', 'B', 'C']替換成縣市選項 
    #district = st.multiselect('請選擇區域', ['a', 'b', 'c', 'd'])
    # 呼叫 getSpecificBookstore 並將回傳值賦值給變數 specificBookstore
    specificBookstore=getSpecificBookstore(bookstorelist, county)
    num = len(specificBookstore)
	# 用 st.write 將目標書店的總數量計算出來，格式：總共有3項結果
    st.write(f'總共有{num}項結果')
    # 呼叫 getBookstoreInfo 並將回傳值賦值給變數 bookstoreInfo
    bookstoreInfo=getBookstoreInfo(specificBookstore)
if __name__ == '__main__':
    app()

# python -m streamlit run app.py

