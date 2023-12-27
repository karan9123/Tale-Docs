CREATE TYPE STATUS AS ENUM ('Active', 'Inactive', 'Deactivated');

CREATE TABLE "user" (
    "id" SERIAL PRIMARY KEY,
    "password" VARCHAR(255) NOT NULL,
    mobile VARCHAR(20),
    user_name VARCHAR(255) NOT NULL UNIQUE,
    fname VARCHAR(50) NOT NULL,
    lname VARCHAR(50) NOT NULL,
    birth_date DATE NOT NULL,
    nick_name VARCHAR(50),
    home_location VARCHAR(255),
    current_location VARCHAR(255),
    device VARCHAR(50) NOT NULL,
    os VARCHAR(50),
    "language" VARCHAR(50),
    timezone VARCHAR(50),
    created_at TIMESTAMP NOT NULL,
    last_online TIMESTAMP NOT NULL,
    gender VARCHAR(10),
    bio TEXT,
    account_status STATUS NOT NULL,
    share_email BOOLEAN NOT NULL,
    share_name BOOLEAN NOT NULL
);


CREATE TABLE relation (
    "id" SERIAL PRIMARY KEY,
    "type" VARCHAR(50) UNIQUE NOT NULL,
    "depth" INTEGER NOT NULL CHECK ("depth" >= -5 AND "depth" <= 5)
);


CREATE TABLE "link" (
    "id" SERIAL PRIMARY KEY,
    user_id_from INTEGER NOT NULL REFERENCES "user"("id"),
    user_id_to INTEGER NOT NULL REFERENCES "user"("id"),
    "type" INTEGER REFERENCES relation("id"),
    created_at TIMESTAMP NOT NULL,
    accepted_at TIMESTAMP NOT NULL,
    terminated_at TIMESTAMP NOT NULL,
    last_edited TIMESTAMP NOT NULL
);