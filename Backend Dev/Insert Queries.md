First 10 Users:
INSERT INTO "user" (user_name, fname, lname, email, birth_date, mobile, nick_name, "password", share_email, share_name, share_phone, created_at, last_online, device, account_status) VALUES
('johnsmith01', 'John', 'Smith', 'johnsmith01@example.com', '1990-01-01', '555-0101', 'Johnny', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('janedoe01', 'Jane', 'Doe', 'janedoe01@example.com', '1992-02-02', '555-0202', 'Janey', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('bobjohnson01', 'Bob', 'Johnson', 'bobjohnson01@example.com', '1991-03-03', '555-0303', 'Bobby', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('alicewhite01', 'Alice', 'White', 'alicewhite01@example.com', '1993-04-04', '555-0404', 'Ally', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('davidbrown01', 'David', 'Brown', 'davidbrown01@example.com', '1989-05-05', '555-0505', 'Dave', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('emmagreen01', 'Emma', 'Green', 'emmagreen01@example.com', '1994-06-06', '555-0606', 'Emmy', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('michaelgray01', 'Michael', 'Gray', 'michaelgray01@example.com', '1990-07-07', '555-0707', 'Mike', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('sarahjones01', 'Sarah', 'Jones', 'sarahjones01@example.com', '1991-08-08', '555-0808', 'Sally', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('jamesmartin01', 'James', 'Martin', 'jamesmartin01@example.com', '1992-09-09', '555-0909', 'Jim', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('lisawilson01', 'Lisa', 'Wilson', 'lisawilson01@example.com', '1993-10-10', '555-1010', 'Lizzy', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active');


INSERT INTO "user" (user_name, fname, lname, email, birth_date, mobile, nick_name, "password", share_email, share_name, share_phone, created_at, last_online, device, account_status) VALUES
('markthomas01', 'Mark', 'Thomas', 'markthomas01@example.com', '1990-11-11', '555-1111', 'Marky', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('nancyharris01', 'Nancy', 'Harris', 'nancyharris01@example.com', '1991-12-12', '555-1212', 'Nan', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('kevinlewis01', 'Kevin', 'Lewis', 'kevinlewis01@example.com', '1992-01-13', '555-1313', 'Kev', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('juliaroberts01', 'Julia', 'Roberts', 'juliaroberts01@example.com', '1993-02-14', '555-1414', 'Julie', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active'),
('tommiller01', 'Tom', 'Miller', 'tommiller01@example.com', '1994-03-15', '555-1515', 'Tommy', 'hashed_password', true, true, true, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, 'IPHONE', 'Active');

INSERT INTO relation ("type", "depth") VALUES 
('father',	1),
('mother',	1),
('brother',	2),
('sister',	2),
('son',	1),
('daughter',	1),
('secondmother',	-1),
('secondfather',	-1),
('stepmother',	-1),
('stepfather',	-1),
('stepsister',	0),
('stepbrother',	0),
('grandmother',	2),
('grandfather',	2),
('best-friend',	0),
('cousin',	0),
('boyfriend',	0),
('girlfriend',	0),
('wife',	0),
('husband',	0),
('grandson', 2),
('granddaughter', 2);



INSERT INTO "link" (user_id_from, user_id_to, "type", created_at, accepted_at, last_edited) VALUES
(1, 2, 21, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 3, 22, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 4, 23, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 5, 24, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 6, 25, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1,7, 33, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 8, 34, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 9, 35, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 10, 39, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 11, 41, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP),
(1, 12, 42, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP);

