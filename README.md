### Hi there 👋

<!--
**Eonly/Eonly** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

a=['H','Li','Na','K','Rb','Cs','Fr']
b=['Be','Mg','Ca','Sr','Ba','Ra']
c=['B','Al','Ga','In','Ti','Uut']
d=['C','Si','Ge','Sn','Pb','Uuq']
e=['N','P','As','Sb','Bi','Uup']
f=['O','S','Se','Te','Po','Uuh']
g=['F','Cl','Br','I','At','Uus']

z=[0,a,b,c,d,e,f,g]

print("我们提供一下两种服务：")
print("    A：检索该元素所在位置")
print("    B：检索该位置对应的元素")
print("    ")
f=str(input("请选择您想要的服务（输入“A”或“B”）："))

if f=='A':
    m=int(1)
    n=int(0)
    k=int(0)

    s=input("请输入你想要判断的元素(英文符号):")

    for m in range(1,8):
        if s=='Fr':
            print("该元素位于第1主族第7周期")
            k=1
            break
        for n in range(0,6):
            if s==z[m][n]:
                if m==1:
                    print("该元素位于第",m,"主族","第",n+1,"周期")
                if m!=1:
                    print("该元素位于第",m,"主族","第",n+2,"周期")
                k=1
                break

    if k==0 :
        print("元素周期表中没有该元素或您检索的为副族元素,请重新输入。")
        
if f=='B':
    x=int(input("请输入第几主族："))
    y=int(input("请输入第几周期："))
    
    if x==1:
        y=y-1
    else:
        y=y-2
    
    print('您检索的元素是：',z[x][y])
        
if f!='A' and f!='B':
    print("很抱歉我们只提供以上两种服务，请您重新选择服务类型。")
