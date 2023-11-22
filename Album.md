#### album_id SERIAL PRIMARY KEY,

#### user_id INT NOT NULL,

#### album_name VARCHAR(255) NOT NULL,

#### album_description TEXT,

#### created_at TIMESTAMP WITH TIME ZONE DEFAULT CURRENT_TIMESTAMP,
#### updated_at TIMESTAMP WITH TIME ZONE DEFAULT CURRENT_TIMESTAMP,
#### share_with_friends BOOLEAN DEFAULT FALSE,

#### FOREIGN KEY (user_id) REFERENCES [[User]](user_id)
