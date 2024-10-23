---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract
The account with the accountname Cbased is the main contract and consists of functions and tables. The order of the parameters is crucial for the integration with the Smart Contract. The developing of the cbased contract is still in process.
## Actions
### addccomment
Type: addccomment

  - **autor** (name)
  - **text** (string)
  - **parentcommentid** (uint64)
  - **language** (string)

### addcomment
Type: addcomment

  - **autor** (name)
  - **text** (string)
  - **uploadid** (uint64)
  - **language** (string)

### addcooldown
Type: addcooldown

  - **autor** (name)
  - **action** (uint16)

### addfavocom
Type: addfavocom

  - **autor** (name)
  - **commentid** (uint64)

### addfavorite
Type: addfavorite

  - **autor** (name)
  - **uploadid** (uint64)

### addfavotag
Type: addfavotag

  - **autor** (name)
  - **globaltagid** (uint64)

### addsubscrip
Type: addsubscrip

  - **autor** (name)
  - **follow** (name)

### addtag
Type: addtag

  - **autor** (name)
  - **uploadid** (uint64)
  - **text** (string)

### addtruster
Type: addtruster

  - **trustername** (name)

### addupload
Type: addupload

  - **autor** (name)
  - **uploadipfshash** (string)
  - **thumbipfshash** (string)
  - **uploadtext** (string)
  - **language** (string)
  - **uploadfiletyp** (string)
  - **thumbfiletyp** (string)
  - **flag** (uint8)

### applytruster
Type: applytruster

  - **autor** (name)
  - **applicationtimeinweek** (uint8)

### banuser
Type: banuser

  - **username** (name)

### claimrewards
Type: claimrewards

  - **autor** (name)
  - **symbol** (string)

### deldm
Type: deldm

  - **autor** (name)
  - **dmid** (uint64)

### delfavocom
Type: delfavocom

  - **autor** (name)
  - **commentid** (uint64)

### delfavorite
Type: delfavorite

  - **autor** (name)
  - **uploadid** (uint64)

### delfavotag
Type: delfavotag

  - **autor** (name)
  - **globaltagid** (uint64)

### delkarma
Type: delkarma

  - **p_truster** (name)

### delsubscrip
Type: delsubscrip

  - **autor** (name)
  - **unfollow** (name)

### delupload
Type: delupload

  - **uploadid** (uint64)

### init
Type: init


### remcooldown
Type: remcooldown

  - **autor** (name)
  - **action** (uint16)

### reportupload
Type: reportupload

  - **autor** (name)
  - **uploadid** (uint64)
  - **violatedrule** (uint8)
  - **reporttext** (string)

### run
Type: run


### senddm
Type: senddm

  - **from** (name)
  - **to** (name)
  - **message** (string)

### setconfig
Type: setconfig

  - **configid** (uint64)
  - **uintvalue** (uint64)
  - **stringvalue** (string)

### setprofile
Type: setprofile

  - **autor** (name)
  - **profilebio** (string)
  - **profileimageipfs** (string)
  - **profileimagefiletyp** (string)
  - **language** (string)
  - **otherconfigsasjson** (string)

### trustervote
Type: trustervote

  - **trustername** (name)
  - **uploadid** (uint64)
  - **vote** (int8)

### votecomment
Type: votecomment

  - **autor** (name)
  - **vote** (int8)
  - **commentid** (uint64)

### votetag
Type: votetag

  - **autor** (name)
  - **vote** (int8)
  - **globuptagid** (uint64)

### voteupload
Type: voteupload

  - **autor** (name)
  - **vote** (int8)
  - **uploadid** (uint64)

## Tables
### badges
Type: badges

  - **badgeid** (uint64)
  - **badgetext** (string)
  - **creationtime** (time_point)
  - **ipfshash** (string)
  - **ipfshash_thumb** (string)
  - **filetyp** (string)

### comments
Type: comments

  - **commentid** (uint64)
  - **parentcommentid** (uint64)
  - **autor** (name)
  - **creationtime** (time_point)
  - **language** (string)
  - **commenttext** (string)
  - **token** (int32)
  - **up** (uint32)
  - **down** (uint32)

### configs
Type: configs

  - **configid** (uint64)
  - **uintvalue** (uint64)
  - **stringvalue** (string)

### cooldown
Type: cooldown

  - **cooldownid** (uint64)
  - **user** (name)
  - **action** (uint16)
  - **counter** (uint16)
  - **lastaction** (time_point)

### dms
Type: dm

  - **messageid** (uint64)
  - **creationtime** (time_point)
  - **autor** (name)
  - **messagetext** (string)

### globaltags
Type: globaltags

  - **globaltagid** (uint64)
  - **creationtime** (time_point_sec)
  - **numoffavorites** (uint64)
  - **trend** (uint64)
  - **numofuploads** (uint64)
  - **up** (uint64)
  - **down** (uint64)
  - **text** (string)

### globcomments
Type: globcomments

  - **commentid** (uint64)
  - **uploadid** (uint64)

### globuptags
Type: globuptags

  - **globuptagid** (uint64)
  - **uploadid** (uint64)

### notifys
Type: notify

  - **notificationid** (uint64)
  - **creationtime** (time_point)
  - **type** (uint16)
  - **notificationtext** (string)

### popular
Type: popular

  - **popularid** (uint64)
  - **uploadid** (uint64)
  - **creationtime** (time_point)

### reports
Type: report

  - **uploadid** (uint64)
  - **reportername** (uint64)
  - **violatedrule** (uint8)
  - **reporttext** (string)
  - **reporttime** (time_point)
  - **numberoftrusters** (uint8)
  - **outstandingvotes** (uint8)
  - **vote_weight** (int8)

### reportvotes
Type: reportvote

  - **trustername** (uint64)
  - **vote** (int8)

### statistics
Type: statistics

  - **id** (uint64)
  - **text** (string)
  - **time** (time_point)
  - **uint64number** (uint64)
  - **int64number** (int64)

### tags
Type: tags

  - **globuptagid** (uint64)
  - **globaltagid** (uint64)
  - **text** (string)
  - **autor** (name)
  - **token** (int32)

### todelete
Type: todelete

  - **id** (uint64)
  - **timetodelete** (time_point_sec)
  - **uploadid** (uint64)

### trusterapply
Type: trusterapply

  - **trustername** (name)
  - **applicationtime** (time_point)
  - **applicationtimeinweek** (uint8)

### trusters
Type: truster

  - **trustername** (uint64)
  - **karma** (uint64)
  - **status** (uint8)
  - **election_date** (time_point)

### uploads
Type: uploads

  - **uploadid** (uint64)
  - **autor** (name)
  - **creationtime** (time_point)
  - **uploadipfshash** (string)
  - **uploadipfshash_filetyp** (string)
  - **thumbipfshash** (string)
  - **thumbipfshash_filetyp** (string)
  - **uploadtext** (string)
  - **language** (string)
  - **flag** (uint8)
  - **numofcomments** (uint32)
  - **numoftags** (uint32)
  - **numoffavorites** (uint32)
  - **token** (uint64)
  - **up** (uint32)
  - **down** (uint32)
  - **popularid** (uint64)

### userbadge
Type: userbadge

  - **userbadgeid** (uint64)
  - **user** (name)
  - **badgeid** (uint64)
  - **handover** (time_point)

### userconfig
Type: userconfig

  - **configid** (uint64)
  - **creationtime** (time_point)
  - **active** (uint8)
  - **last_act_reset** (time_point)
  - **act_token** (uint16)
  - **last_claim_time** (time_point)
  - **istruster** (bool)
  - **numofsubscribtions** (uint16)
  - **numoffollowers** (uint16)
  - **numofuploads** (uint16)
  - **numofcomments** (uint16)
  - **numofuploadvotes** (uint32)
  - **numofcommentvotes** (uint32)
  - **numofaddtags** (uint16)
  - **numoffavorites** (uint16)
  - **numoffavoritetags** (uint16)
  - **numofreports** (uint16)
  - **profilebio** (string)
  - **profileimageipfs** (string)
  - **profileimagefiletyp** (string)
  - **language** (string)
  - **otherconfigsasjson** (string)

### userfavocom
Type: userfavocom

  - **commentid** (uint64)
  - **creationtime** (time_point)

### userfavorite
Type: userfavorite

  - **uploadid** (uint64)
  - **creationtime** (time_point)

### userfavotags
Type: userfavotag

  - **globaltagid** (uint64)

### usersubscrip
Type: usersubscrip

  - **subscriptionid** (uint64)
  - **username** (name)
  - **creationtime** (time_point)

### useruploads
Type: userupload

  - **id** (uint64)
  - **uploadid** (uint64)

### votecomments
Type: votecomments

  - **commentid** (uint64)
  - **vote** (int8)

### votetags
Type: votetags

  - **autor** (name)

### voteuploads
Type: voteuploads

  - **uploadid** (uint64)
  - **vote** (int8)

### withthistag
Type: withthistag

  - **uploadid** (uint64)

