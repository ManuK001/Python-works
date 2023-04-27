

import re

class RegexTest:
    
    def is_valid_email(self, email):
        email_regex = re.compile(r"[^@]+@[^@]+\.[^@]+")
        return bool(email_regex.match(email))
    
    def is_valid_phone_number(self, phone_number):
        phone_regex = re.compile(r"\d{3}-\d{3}-\d{4}")
        return bool(phone_regex.match(phone_number))
    
    def find_all_occurrences(self, file_path, word):
        with open(file_path, "r") as file:
            contents = file.read()
            word_regex = re.compile(r"\b{}\b".format(word))
            return word_regex.findall(contents)
    
    def replace_word(self, file_path, old_word, new_word):
        with open(file_path, "r") as file:
            contents = file.read()
            word_regex = re.compile(r"\b{}\b".format(old_word))
            new_contents = word_regex.sub(new_word, contents)

        with open(file_path, "w") as file:
            file.write(new_contents)
    
    def extract_emails(self, file_path):
        with open(file_path, "r") as file:
            contents = file.read()
            email_regex = re.compile(r"[^@]+@[^@]+\.[^@]+")
            return email_regex.findall(contents)
    
    def extract_phone_numbers(self, file_path):
        with open(file_path, "r") as file:
            contents = file.read()
            phone_regex = re.compile(r"\d{3}-\d{3}-\d{4}")
            return phone_regex.findall(contents)
    
    def remove_non_alphanumeric(self, string):
        alphanumeric_regex = re.compile(r"\W+")
        return alphanumeric_regex.sub("", string)
    
    def format_string(self, string, length):
        if len(string) > length:
            string = string[:length]
        else:
            string += " " * (length - len(string))

        return string
    
    def parse_apache_logs(self, log_file):
        with open(log_file, "r") as file:
            log_data = file.read()
            log_regex = re.compile(r'(\S+) (\S+) (\S+) \[([\w:/]+\s[+\-]\d{4})\] "(\S+) (\S+)\s*(\S+)?\s*" (\d{3}) (\S+)')
            log_entries = log_regex.findall(log_data)
            return log_entries
    
    def parse_json_logs(self, log_file):
        with open(log_file, "r") as file:
            log_data = file.read()
            json_regex = re.compile(r"{.*}")
            log_entries = json_regex.findall(log_data)
            parsed_logs = [json.loads(log) for log in log_entries]
            return parsed_logs

      
