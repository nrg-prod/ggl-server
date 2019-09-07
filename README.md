# Server Info

Server IP : 35.162.40.190

SSL Port number : 22

User Name : ec2-user

# Stop-service

chmod 777 /etc/init.d/gglbootserv

sudo service gglbootserv stop

# Start-service

sudo service gglbootserv start


Connect Mongo DB
================

mongo localhost/admin;

use InvestmentDB;

show databases;

use InvestmentDB;

Update 
=======
Not yet loaded

Remove | Only Data
==================
db.randomNumber.remove( { } );

db.publictree.remove( { } );

db.ownTree.remove( { } );

db.privateTree.remove( { } );

db.tempPublicTree.remove( { } );

db.tempPrivateTree.remove( { } );

db.tempOwnTree.remove( { } );

db.MemberRanomNumber.remove( { } );

db.memberDetails.remove( { } );

Drop collection - do not use in Production
===============
db.randamNumber.drop()

Select Collections ( Table )
=======
db.randomNumber.find();

db.publictree.find();

db.ownTree.find();

db.privateTree.find();


db.tempPublicTree.find();

db.tempPrivateTree.find();

db.tempOwnTree.find();

db.MemberRanomNumber.find();

db.memberDetails.find();

db.publictree.find().sort( { "queueNumber": -1 } );

Insert
=======

db.randomNumber.insertOne( { randomID:1 , currentqueueNumber: 0, nextOutqueueNumber: 7, invocieNumber: 0, invoiceCode: "GSP" } );

db.randomNumber.insertOne( { randomID:2 , currentqueueNumber: 0, invocieNumber: 0, invoiceCode: "GSPR" } );

db.randomNumber.insertOne( { randomID:3 , publicCount: 0, privateCount: 0, ownCount: 0, publicInvCode: "TGSP",privateInvCode: "PGSP",ownInvCode: "OGSP" } );

db.MemberRanomNumber.insertOne( { member_code:"GGLM" , franchise_code:"GGLF",master_franchise_code:"GGLFM", current_member_number: 600800, current_group_number:100, treerandamnumber: 0,consnumber:"GGLRandom" } );

db.memberDetails.insertOne( { member_Number:"GGLFM600800" , member_acct_type:"Platinum",group_name:100, sequance_number: 1, total_commission:0, total_commission: 0 ,level_number:0,tree_name:"A0",total_amount:0,withdraw_status:"None"	} );


Clear
======
Control + l
