---
tags: [curl]
title: gitlab api
created: '2019-07-30T06:19:49.064Z'
modified: '2019-12-30T13:11:54.514Z'
---

# gitlab api

## usage
```sh
X-Total 	                # The total number of items
X-Total-Pages 	          # The total number of pages
X-Per-Page 	              # The number of items per page
X-Page 	                  # The index of the current page (starting at 1)
X-Next-Page 	            # The index of the next page
X-Prev-Page   	          # The index of the previous page
private-token: TOKEN      # token..
```

```sh
GET "/api/v4/projects/8/issues/8/notes?per_page=3&page=2"

GET "/api/v4/projects/?private_token=TOKEN&per_page=2&page=1"

# get projects with a schedule
GET "HOST/api/v4/projects?simple=true&per_page=100"             | awk 'BEGIN {FS=": "}/^X-Total-Pages/{print $2}'

GET "HOST/api/v4/projects?simple=true&per_page=100&page=${page}" | jq '.[].id'

curl --no-buffer -s "HOST/api/v4/projects/${id}" | jq '.name'

curl --no-buffer -s "HOST/api/v4/projects/${id}/pipeline_schedules" | jq '.'


# namespace
GET "/api/v4/namespaces?per_page=100" | jq '.[] | select(.kind=="group") | "\(.id) \(.path)"'     # get system namespaces


# groups
GET "/groups/:id/projects"
GET "/api/v4/groups/26/projects" | jq -r '.[].ssh_url_to_repo'      # ssh project url from namespace-id if group

# runners
GET "/api/v4/runners"
GET "/api/v4/runners/161"
GET "/api/v4/runners/all?status=active"

DELETE "/api/v4/runners/161"
```

## see also
- [[gitlab-runner]]
- [[git]]
- [[curl]]
- [GitLab API | GitLab](https://docs.gitlab.com/ee/api/README.html#basic-usage)
