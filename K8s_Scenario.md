1. “ 𝗬𝗼𝘂𝗿 𝗖𝗜/𝗖𝗗 𝗽𝗶𝗽𝗲𝗹𝗶𝗻𝗲 𝗽𝗮𝘀𝘀𝗲𝗱. 𝗕𝘂𝘁 𝗣𝗿𝗼𝗱 𝘀𝘁𝗶𝗹𝗹 𝗵𝗮𝘀 𝗼𝗹𝗱 𝗰𝗼𝗱𝗲. 𝗘𝘅𝗽𝗹𝗮𝗶𝗻. ”

My answer: I have seen this before. Here is exactly why.

► Pipeline passed — but deployment step may have been skipped.
 Check pipeline logs — did deploy stage actually run?

► Wrong environment — pipeline deployed to Staging not Production.
 Check deploy script — which environment variable is set?

► Cache issue — browser or CDN is serving cached old version.
 Hard refresh: Ctrl + Shift + R — check if new code appears.
 Invalidate CloudFront cache if using CDN.

► Health check rollback — new deployment failed health check.
 Load balancer silently rolled back to old version.
 Check ALB target group — which version is active?

► Wrong image tag — deployment pulled latest but latest was not updated.
 Always use specific image tags. Never use :latest in production.

► Blue-Green switch missed — new version deployed but traffic not switched.
 Check load balancer listener rules.

𝗛𝗼𝘄 𝗜 𝘀𝗲𝘁 𝘂𝗽 𝗯𝘂𝗹𝗹𝗲𝘁𝗽𝗿𝗼𝗼𝗳 𝗖𝗜/𝗖𝗗:
• Add smoke test after deployment — verify new version is live
• Use specific image tags — never :latest in production
• Add deployment verification step in pipeline
• Set up CloudWatch alarm on deployment events
• Always check target group after blue-green switch
