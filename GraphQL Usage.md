

query TEstQuery($userId: Int!){

user(userId: $userId) {

user_id

user_email

user_fname

user_lname

user_birth_date

user_name

}

TierOne(userId: $userId) {

related_to

groups

relation_name

user_name

}

TierTwo(userId: $userId) {

related_to

groups

relation_name

user_name

}

TierThree(userId: $userId) {

related_to

groups

relation_name

user_name

}

}