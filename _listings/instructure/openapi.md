swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Utility APIs
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/group_categories:
    get:
      summary: List group categories for a context
      description: List group categories for a context.
      operationId: list-group-categories-for-a-context
      x-api-path-slug: coursescourse-idgroup-categories-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Group
      - Categories
    post:
      summary: Create a Group Category
      description: Create a group category.
      operationId: create-a-group-category
      x-api-path-slug: coursescourse-idgroup-categories-post
      parameters:
      - in: query
        name: auto_leader
        description: 'Assigns group leaders automatically when generating and allocating
          studentsnto groups Valid values are:nu201cfirstu201dnnthe first student
          to be allocated to a group is the leadernu201crandomu201dnna random student
          from all members is chosen as the leadernnn        n        n          Allowed
          values: first, random'
      - in: query
        name: create_group_count
        description: Create this number of groups (Course Only)
      - in: query
        name: group_limit
        description: Limit the maximum number of users in each group (Course Only)
      - in: query
        name: name
        description: Name of the group category
      - in: query
        name: self_signup
        description: Allow students to sign up for a group themselves (Course Only)
      - in: query
        name: split_group_count
        description: (Deprecated) Create this number of groups, and evenly distribute
          studentsnamong them
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Group
      - Categories
  /group_categories/{group_category_id}:
    delete:
      summary: Delete a Group Category
      description: Delete a group category.
      operationId: delete-a-group-category
      x-api-path-slug: group-categoriesgroup-category-id-delete
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
    get:
      summary: Get a single group category
      description: Get a single group category.
      operationId: get-a-single-group-category
      x-api-path-slug: group-categoriesgroup-category-id-get
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
    put:
      summary: Update a Group Category
      description: Update a group category.
      operationId: update-a-group-category
      x-api-path-slug: group-categoriesgroup-category-id-put
      parameters:
      - in: query
        name: auto_leader
        description: 'Assigns group leaders automatically when generating and allocating
          studentsnto groups Valid values are:nu201cfirstu201dnnthe first student
          to be allocated to a group is the leadernu201crandomu201dnna random student
          from all members is chosen as the leadernnn        n        n          Allowed
          values: first, random'
      - in: query
        name: create_group_count
        description: Create this number of groups (Course Only)
      - in: query
        name: group_limit
        description: Limit the maximum number of users in each group (Course Only)
      - in: query
        name: name
        description: Name of the group category
      - in: query
        name: self_signup
        description: Allow students to sign up for a group themselves (Course Only)
      - in: query
        name: split_group_count
        description: (Deprecated) Create this number of groups, and evenly distribute
          studentsnamong them
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
  /group_categories/{group_category_id}/assign_unassigned_members:
    post:
      summary: Assign unassigned members
      description: Assign unassigned members.
      operationId: assign-unassigned-members
      x-api-path-slug: group-categoriesgroup-category-idassign-unassigned-members-post
      parameters:
      - in: query
        name: sync
        description: The assigning is done asynchronously by default
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
      - Assign
      - Unassigned
      - Members
  /group_categories/{group_category_id}/groups:
    get:
      summary: List groups in group category
      description: List groups in group category.
      operationId: list-groups-in-group-category
      x-api-path-slug: group-categoriesgroup-category-idgroups-get
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
      - Groups
    post:
      summary: Create a group
      description: Create a group.
      operationId: create-a-group
      x-api-path-slug: group-categoriesgroup-category-idgroups-post
      parameters:
      - in: query
        name: description
        description: A description of the group
      - in: query
        name: is_public
        description: whether the group is public (applies only to community groups)
      - in: query
        name: join_level
        description: 'no descriptionnn        n        n          Allowed values:
          parent_context_auto_join, parent_context_request, invitation_only'
      - in: query
        name: name
        description: The name of the group
      - in: query
        name: storage_quota_mb
        description: The allowed file storage for the group, in megabytes
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
      - Groups
  /group_categories/{group_category_id}/users:
    get:
      summary: List users in group category
      description: List users in group category.
      operationId: list-users-in-group-category
      x-api-path-slug: group-categoriesgroup-category-idusers-get
      parameters:
      - in: query
        name: search_term
        description: The partial name or full ID of the users to match and return
          in the resultsnlist
      - in: query
        name: unassigned
        description: Set this value to true if you wish only to search unassigned
          users in thengroup category
      responses:
        200:
          description: OK
      tags:
      - Group
      - Categories
      - Group
      - Category
      - Id
      - Users
  /users/self/communication_channels/{communication_channel_id}/notification_preference_categories/category:
    put:
      summary: Update preferences by category
      description: Update preferences by category.
      operationId: update-preferences-by-category
      x-api-path-slug: usersselfcommunication-channelscommunication-channel-idnotification-preference-categoriescategory-put
      parameters:
      - in: query
        name: category
        description: The name of the category
      - in: query
        name: notification_preferences[frequency]
        description: The desired frequency for each notification in the category
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Communication
      - Channels
      - Communication
      - Channel
      - Id
      - Notification
      - Preference
      - Categories
      - Category
  /users/{user_id}/communication_channels/communication_channel_id/notification_preference_categories:
    get:
      summary: List of preference categories
      description: List of preference categories.
      operationId: list-of-preference-categories
      x-api-path-slug: usersuser-idcommunication-channelscommunication-channel-idnotification-preference-categories-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - User
      - Id
      - Communication
      - Channels
      - Communication
      - Channel
      - Id
      - Notification
      - Preference
      - Categories