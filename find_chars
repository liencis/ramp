import base64

def decode_s(s):
    string = s
    decoded_s = base64.b64decode(string)
    result = decoded_s.decode('utf-8')

    print(result)

s = "aHR0cHM6Ly90bnM0bHBnbXppaXlwbnh4emVsNXNzNW55dTBuZnRvbC5sYW1iZGEtdXJsLnVzLWVhc3QtMS5vbi5hd3MvcmFtcC1jaGFsbGVuZ2UtaW5zdHJ1Y3Rpb25zLw=="
decode_s(s)
    
def get_url_char(x_list, ref):
    for s in x_list:
        s_list = s.split('"')
        for i, el in enumerate(s_list):
            if el == 'ref':
                ref += s_list[i + 2]
    return ref
# Copied HTML out form "insigts" from browswer 
# formated it in lines like nice HTML and saved it in find.txt file
with open("find.txt") as f:
    ref = ""
    for x in f:
        if '<b class="ramp ' in x:
            x_list = x.split('<b class="ramp ')[1:]
            ref = get_url_char(x_list, ref)

    print(ref)
