
#### phototag_id INT AUTO_INCREMENT PRIMARY KEY,
#### photo_id INT,

#### tagged_user_id INT,
#### tag_x_coordinate FLOAT,
#### tag_y_coordinate FLOAT,
#### created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
#### FOREIGN KEY (photo_id) REFERENCES [[Photos]](photo_id),
#### FOREIGN KEY (tagged_user_id) REFERENCES [[User]](user_id)