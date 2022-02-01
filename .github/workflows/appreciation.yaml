name: Appreciation
issues:
  types: [ opened ]

jobs:
  appreciation:
    name: Appreciation
    runs-on: ubuntu-latest
    steps:
      - uses: bluenovaio/action-slack@main 
        with:
          username: "Appreciation Bot"
          icon_emoji: ":robot_face:"
          if: contains(github.event.pull_request.labels.*.name, 'appreciation')
          text: |
            ${{ github.event.issue.title }}
            
            ${{ github.event.issue.body }}

            Sent by: ${{ github.event.issue.user.login }}
        
          webhook_url: ${{ secrets.SLACK_WEBHOOK_URL }} 
