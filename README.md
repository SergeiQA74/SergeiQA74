## Hi there 👋 I'm Sergei,:man_technologist: Now About Me :
## I am a QA Manual and Automation Engineer <img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="47">
## - :telescope: I’m working as a QA Software Engineer with different Languages(Python,JavaScript,SQL,HTML),services and programs.
## - :seedling: I finished the QA at Silicon Valley School(California).
## - :zap: In my free time, I like to play tennis, go fishing and training at the gym .
## - :mailbox:How to find me:<div id="badges">
  <a href="https://www.linkedin.com/in/sergei-kutnyi/">
  <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
<div align="center">
  <img src="https://media.giphy.com/media/dWesBcTLavkZuG35MI/giphy.gif" width="600" height="300"/>
</div>

## Don't worry if something doesn't work. If everything worked, I would be fired.
![beautiful](https://i.pinimg.com/736x/38/42/d3/3842d3ad2fd6ebbf9376d10f70498a23--desk-setup-work-spaces.jpg)

<img src="https://SergeiQA74/ghpvc/?username=your-github-username&style=flat-square&color=blue" alt=""/>

 ## :hammer_and_wrench: Languages and Tools :
  <div>
  <img src=https://github.com/devicons/devicon/blob/master/icons/python/python-original-wordmark.svg title="Python" alt="Python" width="45" height="45"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="45"       height="45"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/css3/css3-plain-wordmark.svg"  title="CSS3" alt="CSS" width="45" height="45"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL"  alt="MySQL" width="45" height="45"/>&nbsp; 
  <img src="https://github.com/devicons/devicon/blob/master/icons/nodejs/nodejs-original-wordmark.svg" title="NodeJS" alt="NodeJS" width="55" height="55"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/webstorm/webstorm-original-wordmark.svg" title="Webstorm" alt="Webstorm" width="55" height="55"/>&nbsp;

const fs = require('fs');
const jsYaml = require('js-yaml');
const axios = require('axios');

const LANGS_FILEPATH = "./src/common/languageColors.json"

//Retrieve languages from github linguist repository yaml file
//@ts-ignore
axios.get("https://raw.githubusercontent.com/github/linguist/master/lib/linguist/languages.yml")
.then((response) => {

  //and convert them to a JS Object
  const languages = jsYaml.load(response.data);

  const languageColors = {};

  //Filter only language colors from the whole file
  Object.keys(languages).forEach((lang) => {
    languageColors[lang] = languages[lang].color;
  });

  //Debug Print
  //console.dir(languageColors);
  fs.writeFileSync(LANGS_FILEPATH, JSON.stringify(languageColors, null, '    '));
  
});    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
