# deepl-cli

My own reinvention of the wheel that let's you translate text from commandline using deepl API. 

In order to use it, you will need to obtain the API key from the deepl site (https://www.deepl.com/pl/pro-api?cta=header-pro-api/). Once you obtain the key create the `.apikey.txt` file in the same current working directory, and place it there. Also make the deepl-cli program executable by `chmod +x deepl-cli` command. 

You can also place the deepl-cli file somewhere on your $PATH, so you can invoke it from anywhere

Run the `pip install deepl` in order to download the deepl python library

### Usage

Use: `./deepl-cli -usage` in order to informations about your current API usage (number of characters that were translated, in the free api subscription, the monthly limit is 500 000 )

Use: `./deepl-cli -f file_name` replace the  file_name with the name of the file that you want to translate text from. It will print the output to the stdout. If you want to create the translated file, use redirection `./deepl-cli -d file_name > translated_file_name`

You can also pipe the text or content of the file to the the deepl-cli

By default it is autodetecting the text and translating it into english, if you want to specify another language, use: `./deepl-cli -l language_of_your_choice`. Currently supported languages: { english, polish }
