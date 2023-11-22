## User
CREATE TABLE users (
    user_id SERIAL PRIMARY KEY,
    user_name VARCHAR(255) UNIQUE NOT NULL,
    user_fname VARCHAR(255) NOT NULL,
    user_lname VARCHAR(255) NOT NULL,
    user_email VARCHAR(255) UNIQUE NOT NULL,
    user_birth_date DATE NOT NULL,
    user_mobile VARCHAR(255),  -- Assuming only one primary mobile number
    user_nick_name VARCHAR(255),
    user_pass VARCHAR(255) NOT NULL,  -- Storing hashed password
    photo_id INTEGER,  -- Foreign key to the Photos table (optional)
    user_share_email BOOLEAN NOT NULL,
    user_share_usern BOOLEAN NOT NULL,
    current_location VARCHAR(255),
    home_location VARCHAR(255),
    user_share_phone BOOLEAN NOT NULL,
    user_created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    user_last_online TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);
## Relationship

CREATE TABLE relationships (
    relationship_id SERIAL PRIMARY KEY,
    user_id_from INTEGER REFERENCES users(user_id),
    user_id_to INTEGER REFERENCES users(user_id),
    relationship_type VARCHAR(255) NOT NULL
);



## Photo
CREATE TABLE photos (
    photo_id SERIAL PRIMARY KEY,
    photo_title VARCHAR(255),
    photo_desc TEXT,
    photo_url VARCHAR(255) NOT NULL,
    user_id INTEGER REFERENCES users(user_id),
    created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    photo_date DATE,
    photo_geo VARCHAR(255),
    photo_album VARCHAR(255),
    thumbnail_url VARCHAR(255),
    is_public BOOLEAN NOT NULL
);

## PhotoUserTagged

CREATE TABLE photo_user_tagged (
    phototag_id SERIAL PRIMARY KEY,
    photo_id INTEGER REFERENCES photos(photo_id),
    tagged_user_id INTEGER REFERENCES users(user_id),
    tag_x_coordinate FLOAT,
    tag_y_coordinate FLOAT,
    created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);

## Album 
CREATE TABLE albums (
    album_id SERIAL PRIMARY KEY,
    user_id INTEGER REFERENCES users(user_id),
    album_title VARCHAR(255),
    album_desc TEXT,
    album_date DATE,
    album_pub BOOLEAN NOT NULL,
    created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);


