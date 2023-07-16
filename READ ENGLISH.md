**Caution**<br>
_Only `summon.sf` located in the same directory will be recognized!<br>It won't recognize any file with a different name!_<br>
To be patched.

# How to Use SF Script (Summon File Script)

![sf script](https://github.com/newhajinyoon/sf-script/assets/61103309/dee7e8d5-16d8-49de-918c-e6d41ac6471a)

**SF Script** is a command script that automatically generates files and code. You can create or overwrite files and code following the provided commands. When used in conjunction with GPT, its effectiveness increases by 2051 times.

1. [Download](https://github.com/newhajinyoon/sf-script/releases) the SF Script.
2. Place the `sf.exe` file in the same directory as the prepared `summon.sf` file.
3. Run `sf.exe`.

## Writing Command Scripts

1. `m : path;`: Set the default path for file creation. All subsequent files and directories will be created relative to this base path.

2. `f : filename;`: Create a file. The filename represents the relative path of the file to be created, based on the default path. If the filename includes subdirectories, they will be automatically created if they don't exist.

3. Overwriting code:
   ```
   c[filename] :
   --!
   code
   --!;
   ```
   This overwrites the content of a file. Specify the relative path of the file to be overwritten in `[filename]`, and write the content to be overwritten in the `code` section.

4. `;`: The semicolon denotes the end of a command. Each command is separated by semicolons.

5. '*' : Annotation.

6. 'l : true' : When writing at the beginning of the code, 'log.txt' is generated.

## Example

Below is an example of an `.sf` script that can be copied into a "summon.sf" file for use:

```sf
m : D:\desktop\python\summon;

f : templates/hi.html;
f : templates/test.html;
f : app.py;
f : data.json;

c[templates/test.html] : 
--!
<div> This is the in-game template </div>
--!;

c[templates/hi.html] : 
--!
<p> hi! </p>
--!;
```

## Utilizing with GPT

When using `.sf` files together with GPT, you can create a **wide variety of websites** within 30 seconds.

Here's an example of asking GPT to create a simple chat website using Flask and requesting it to generate at least 5 files, utilizing the SF Script:

```
Create an online chat service with Flask, include CSS, and generate at least 5 files. Use SF Script to do this.
```



https://github.com/newhajinyoon/sf-script/assets/61103309/26542a1a-bdfc-4317-8b1c-608c2274769c



You can download the resulting `summon.sf` file [here](https://github.com/newhajinyoon/sf-script/blob/main/example/chat/summon.sf).

### Teaching GPT the SF Script

To teach GPT, copy all the text from [here](https://raw.githubusercontent.com/newhajinyoon/sf-script/main/GPT/V1%20en) and paste it into GPT. After GPT has learned, simply append a request to use the SF Script at the end of your input, and it will work. <br>
[Korean Version](https://raw.githubusercontent.com/newhajinyoon/sf-script/main/GPT/V1)

## Planned Features

Implementation of a feature to execute the SF file simply by clicking on it will be included in the upcoming plans.

<span style="color:red">
