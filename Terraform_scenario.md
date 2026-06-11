1. 𝗜𝗻𝘁𝗲𝗿𝘃𝗶𝗲𝘄𝗲𝗿: 𝗬𝗼𝘂 𝗵𝗮𝘃𝗲 𝟮 𝗺𝗶𝗻𝘂𝘁𝗲𝘀. 𝗧𝗲𝗿𝗿𝗮𝗳𝗼𝗿𝗺 𝗮𝗽𝗽𝗹𝘆 𝗳𝗮𝗶𝗹𝗲𝗱 𝗵𝗮𝗹𝗳𝘄𝗮𝘆. 𝗜𝗻𝗳𝗿𝗮𝘀𝘁𝗿𝘂𝗰𝘁𝘂𝗿𝗲 𝗶𝘀 𝗯𝗿𝗼𝗸𝗲𝗻. 𝗪𝗵𝗮𝘁 𝗱𝗼 𝘆𝗼𝘂 𝗱𝗼?

My answer: Challenge accepted, let’s go!

► Partial apply means state file is now out of sync with real infrastructure.

► First — do NOT run terraform apply again immediately. It can make things worse.

► State mismatch — some resources created, some not. State file shows incomplete picture.

► Locked state — if using S3 + DynamoDB, state may still be locked. Release it first:
 terraform force-unlock LOCK-ID

► Check what failed — read the exact error message carefully. Fix the root cause first.

► Refresh state — sync state file with real infra:
 terraform refresh

► Import missing resources — if resource exists in AWS but not in state:
 terraform import aws_instance.web i-1234567890

► Run terraform plan — see exactly what will change before applying again.

► Then run terraform apply — only after plan looks correct.

𝗛𝗼𝘄 𝗜 𝗽𝗿𝗲𝘃𝗲𝗻𝘁 𝘁𝗵𝗶𝘀 𝗮𝘀 𝗮 𝗗𝗲𝘃𝗢𝗽𝘀 𝗘𝗻𝗴𝗶𝗻𝗲𝗲𝗿:
• Always use remote state with S3 + DynamoDB locking
• Never run apply directly — always plan first
• Use workspaces to separate environments
• Enable versioning on S3 state bucket
• Use terraform validate in CI/CD before apply

##
