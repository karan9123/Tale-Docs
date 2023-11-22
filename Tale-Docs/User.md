

```mermaid
erDiagram

 User {
    Int id
    VARCHAR(50) name
    VARCHAR(255) user_fname
    VARCHAR(255)  user_lname
    VARCHAR(100)  user_email
    DATE user_birth_date
    VARCHAR(15) user_mobile
    VARCHAR(50) user_nick_name
    HashKey(TBD) user_password
    VARCHAR(255) user_profile_picture
    BOOLEAN  user_share_usern
    BOOLEAN user_share_phone
    TEXT user_status
    dateTime user_created_at
    dateTime user_last_online
} 

```



#### user_id SERIAL PRIMARY KEY,
#### user_name VARCHAR(50),

#### user_fname VARCHAR(50),
#### user_lname VARCHAR(50),

#### user_email VARCHAR(100) UNIQUE NOT NULL,
#### user_birth_date DATE,

#### user_mobile VARCHAR(15), 

#### user_nick_name VARCHAR(50), 

##### user_password HashKey(TBD)

##### user_profile_picture VARCHAR(255), -- URL to the image stored on S3.

#### user_share_usern BOOLEAN NOT NULL DEFAULT false, 

#### user_share_phone BOOLEAN NOT NULL DEFAULT false
#### user_status (text) To set a status message
#### user_created_at (dateTime)

#### user_last_online (dateTime)

#### privacy_settings


