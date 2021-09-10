var fs = require("fs");                 //accessing/requiring the file system       

fs.mkdirSync("nishant");                   //creating the folder --> nishant
fs.writeFileSync("nishant/hello.txt","Hello from demo",(err) => {           //creating the file --> hello
    if(err){
        console.log(err);
    }
});

var data = fs.readFileSync("nishant/hello.txt","utf-8");                    //reading the file hello.txt and fetching it in data
console.log(data);                                                       //printing data

fs.appendFileSync("nishant/hello.txt",",this is the appended text");           //appending some text in hello.txt file
data = fs.readFileSync("nishant/hello.txt","utf-8");
console.log(data);

fs.renameSync("nishant/hello.txt","nishant/hello2.txt");                          //renamed the file

fs.unlinkSync("nishant/hello2.txt");                                           //file deleted

fs.rmdirSync('nishant');                                                       //folder/schema deleted
