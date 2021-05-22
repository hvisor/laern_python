import re
txt = 'What kind of music do you like?'
rep = {"a": "", "e": "", "i": "", "o": "", "u": ""}
pattern = re.compile("|".join(rep.keys()))
txt = pattern.sub(lambda m: rep[re.escape(m.group(0))], txt)

print(txt)
# # # # # # # # # # # # # # # # # # 



txt = 'What kind of music do you like?'
for r in (("a", ""), ("e", ""), ("i", ""), ("o", ""), ("u", "")):
    txt = txt.replace(*r)

print(txt)
# # # # # # # # # # # # # # # # # # 
