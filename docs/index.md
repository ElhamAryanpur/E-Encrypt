## LEGENDS:
    `` is used to show a code!

## USAGE:
    Import it in your desired language (according to my knowledge, any
                                        language that can compile can use
                                        this library!)
    
    First of everything, import the library:

    `import encryptor`
    
    The whole encryptor is a Class object:

    `my_encryptor = encryptor.Encryptor()`

## SALT:
        salt is needed in almost all functions of this tool!
        `my_salt = my_encryptor.encrypt_salt(<Salt>)`
    
## STRING ENCRYPTION:
        string encryption is used to encrypt a string object!
        `my_encrypted_string = my_encryptor.encrypt_string(<salt>, <string to encrypt>)`

## STRING DECRYPTION:
        string decryption is used to decrypt previously encrypted string!
        `my_decrypted_string = my_encryptor.decrypt_string(<salt>, <encrypted string>)`
    
## FILE ENCRYPTION:
        file encryption is used to encrypt a file!
        `my_encryptor.encrypt_file(<salt>, <the file to be encrypted>, <the file that encryption should be written>)`
    
## FILE DECRYPTION:
        file decryption is used to encrypt a file!
        `my_encryptor.decrypt_file(<salt>, <the file that is encrypted>, <the file that decryption should be written>)`

    
## FILE VERSIONING:

        is used to control changes that is made to a file!

## INIT:
            First of all you need to initialize so that it save it in file database!
            `my_encryptor.init_file_history(<salt>, <file to version>, <name of database>, encrypt=<True if you want encryption or False if you don't!>)`
        
## VERIFY:
            after you initialized, you can verify if the file has stayed the same or not!
            this function return a boolean as True if it is same or False if it is not the same!
            `verification = my_encryptor.file_verify(<salt>, <file that is versioned>, <name of database>, encrypt=<True if you did encrypt the database or False if you didn't!>`
        
## ROLLBACK:
            use this if you want to bring back all the changes of a file to the version you initialized!
            `my_encryptor.roll_back(<salt>, <file that is versioned>, <name of database>, encrypt=<True if you did encrypt the database or False if you didn't!>`
    

## NOTE:
    encrypted objects are NOT byte objects! so you can deal with them just like regular
    strings! Salts are encrypted 5 times and strings are encrypted 10 times!

    Examples above can be directly used in python (more specificly python 3.7)!
