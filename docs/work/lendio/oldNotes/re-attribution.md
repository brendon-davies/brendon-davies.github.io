here's a query to use to re-attribute borrowers. it updates the borrowers and marketing table. you need to do a little bit of investigation to determine which specific marketing id's to use for the query, but after you have those. you just need to plug in those values and the affiliate id and the query is good to go to run.


UPDATE
    marketing AS m,
    borrowers AS b,
    affiliates AS a
SET
    m.affiliateId = a.affiliateId,
    m.medium = a.medium,
    m.source = a.name,
    m.partnerOwnedDays = a.ownedDays,
    m.partnerOwnedStart = m.created,
    m.partnerOwnedEnd = (m.created + INTERVAL a.ownedDays DAY),
    m.hasOwnership = 1,
    m.modified = NOW(),
    b.leadMedium = a.medium,
    b.leadSource = a.name,
    b.partnerOwnedDays = a.ownedDays,
    b.partnerOwnedStart = m.created,
    b.partnerOwnedEnd = (m.created + INTERVAL a.ownedDays DAY),
    b.modified = NOW()
WHERE
    b.id = m.borrowerId
    AND m.id IN (3469034, 3469022, 3485966) -- specific marketingIds to update go here 
    AND a.affiliateId = 1539022715; --put the affiliateId the borrowers are to be re-attributed to