SELECT * FROM users u
JOIN listings l
ON u.user_id = l.lister_id
ORDER BY created
where u.user_id IN 
(
SELECT COUNT(user_id) FROM
(SELECT user_id,COUNT(*) as tot FROM users u
JOIN listings l
ON u.user_id = l.lister_id
GROUP BY user_id
)
where tot >= 2)