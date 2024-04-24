#!/usr/bin/env python3
from pymongo import MongoClient, errors
import os
MONGOPASS = os.getenv('MONGOPASS')
uri = "mongodb+srv://cluster0.pnxzwgz.mongodb.net/fhy9gs"
client = MongoClient(uri, username='nmagee', password=MONGOPASS, connectTimeoutMS=200, retryWrites=True)
db = client["lab_9"]
collection = db["lab_9_collection"]
documents = [
    {"name": "Parrot", "color": "Red", "habitat": "Rainforest"},
    {"name": "Alpaca", "color": "White", "habitat": "Mountaineous areas"},
    {"name": "Dolphin", "color": "Blue", "habitat": "Ocean"},
    {"name": "Giraffe", "color": "Brown Spotted", "habitat": "Arid regions"},
    {"name": "Turtle", "color": "Green", "habitat": "ponds"}
]
collection.insert_many(documents)
result = collection.find().limit(3)
for documents in result:
print(documents)
