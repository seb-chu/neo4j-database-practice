- Family tree
  - Family
    - Displays only one ancestral tree
    - User: Node
      - HASH includes NAME, EMAIL**** //not needed for our case just need id.
      - MEDICAL ISSUES (MUST ADD) :)
      - Wishlist/ Wedding registry : )))
      - email 
      - password hash NEEDED
      - Residency: str NODE opt
      - Occupation: str NODE opt
      - Bio: str
      - Picture: url
      - Sex: str 
      - Name: str NEEDED
      - Shirt Size: str
      - people linked by accounts (both are linked to parent, but show 1 depending on family lineage)
        - Conflict
          - if 2 users requested the same person more than once, add warning
        - user request permission from admin to over-write placeholder node and join family tree
          - admin compares placeholder data with requested user data
        - if no placeholder
          - user can create their own placeholder and request permission from admin
      - Important Dates
        - Birthday: date
        - Deathday: date
        - Marriage Anniversary: date
      - Inclusivity
        - Gender: str
        - Pronouns: str with validation (check for two `/` e.g., `he/him/his`)
          - Templates
          - Freeform
        - Private (User-based) View
          - Preferred Guardian Titles: str
            - Ex. Mother (is based off of sex (F)) becomes Parent (larger catagory)
          - Preferred Ancestor Titles: str
            - Ex. Daughter becomes Child (larger category)
      - Socials
        - Email: str
        - Phone number: str with validation (+1 000-000-0000)
        - Social medias: str
          - shows logo and profile name of specific social media (code only)
          - Supported sites
            - Instagram
            - Twitter
            - Facebook
            - Tiktok
            - Linkedin
            - Other websites
      - Relationships: Edge
        - has child
          - List of children
        - married to
          - Person
        - has parent
          - List of parents
      - Personal Notes of other people (Title/Nickname): Edge label
        - created_by: User
        - references: User
        - Nickname (like saying Olive lim == "Po-Po", or 2-cow goong == the flash guy)
        - Personal accounts (ex. inside jokes)
  - Security
    - Sharing
      - Share link of immediate family only
    - Privacy options
      - Guest (without account)
        - Shows only first name, pronouns, gender
      - Family (with account)
        - Shows whole tree
    - encrypt database
- Aggregated Social media feed
  - notifications for special dates
  - favorited people for more of their feed (favorites).
- Calendar
  - Dates from database
- Skill Tree
  - Rank up in milestone as you decay 
    - ex. highschool, college, death.

    --------------------------------------------------------------------------------------

  - Node movement 
    - if leaf node has no children, then it can move around to other parent nodes, 
      -otherwise, the leaf node will be locked in, but ids can change.
    OR
    - if a node is deleted, then do not shift anything, but replace node with "deleted" placeholder node.
  
  - MINIMUM Node API requirements
    - Parent, Child, Spouse, Sibling. (will need api controller for each one).
    - controller endpoints: get one -> "parents, children, siblings",
                            put (update), 
                            delete, 
                            post.
    - step-"whatever" will be a T/F on relationship attribute.