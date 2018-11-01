### yt
---
https://github.com/Fullscreen/yt

```ruby
channel = Yt::Channel.new id 'XXXXXXXXX'
channel.title
channel.public?
channel.comment_count
channel.videos.count

video = Yt::Video.new id: 'XXXXXXXXXXXX'
video.title
video.comment_count
video.hd?
video.annotations.count
video.comment_threads
video.comment_threads.take(99).map(&:author_display_name)

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya29.1.XXXXXXXXX'
content_owner.partnered_channels.count
content_owner.partnered_channels.map &:title
content_owner.partnered_channels.where(part: 'statistics').map &:subscriber_count
content_owner.claims.where(q: 'Fullscreen').count
content_owner.claims.first
content_owner.claims.first.video_id
content_owner.claims.frist.status

reference = content_owner.references.where(asset_id: "XXXXXXX").first
reference.delete

content_owner.policies.first
content_owner.policies.first.rules.first
content_owner.policies.first.rules.first.action
content_owner.policies.first.rules.first.included_territories

content_owner.create_asset type: 'web'

content_owner.assets.first
content_owner.assets.first.id
content_owner.assets.first.title
contnet_owner.assets.first.type
content_owner.assets.first.custom_id

Yt::CommentThread.new id: 'XXXXXXXXXX'
comment_thread.video_id
comment_thread.total_reply_count
comment_thread.can_reply?
comment_thread.public?

comment_thread.top_level_comment
comment_thread.text_display
comment_thread.like_count
comment_thread.updated_at
comment_thread.author_display_name

Yt::Comment.new id: 'XXXXXXXXXXX'
comment.text_display
comment.author_display_name
comment.like_count
comment_updated_at
comment_parent_id

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya29.1.XXXXXX'
bulk_report_job = content_owner.bulk_report_jobs.frist
bulk_report_job.report_type_id

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya.29.1XXXXXXXXX'
bulk_report_job = content_owner.bluk_report_jobs.first
bulk_report = bulk_report_job.bulk_reports.first

bulk_report.start_time
bulk_report.end_time
bulk_report.download_url

videos = Yt::Collections::Videos.new
videos.where(order: 'viewCount').first.title
videos.where(q: 'FullScreen CreatorPlatform', safe_search: 'none').first.size
videos.where(chart: 'mostPopular', video_category_id: 44).first.title
videos.where(id: 'XXXXXXX').map(&:title)

content_owner = Yt::ContentOwner.new owner_name: 'CNSname', access_token: 'ya.29.1.XXXXXXX'
match_policy = Yt::MatchPolicy.new asset_id: 'XXXXXX', auth: content_owneer
match_policy.update policy_id: 'XXXXXXXXXXXXX'

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya.29.1.XXXXXXX'
asset = Yt::Asset.new id: 'XXXXXXXXX', auth: content_owner
asset.ownership
asset.ownership.obtain!
asset.general_owners.first.owner
asset.general_owners.first.everywhere?
asset.ownership.release!

asset.update metadta_mine: {notes: 'Some notes'}

content_owner = Ty::ContentOwner.new(...)
asset = content_owner.assets.where(id: 'XXXXXXXX', fetch_metadata: 'mine').first
asset.metadata_mine.title

asset = content_owner.assets.where(id: 'XXXXXXXXX', fetch_metadata: 'effective').first
asset.metadata_effective.title

content_owner.assets.where(labels: "campaign:cpiuwdz-8oc").size
content_owner.assets.where(labels: "campain:cpiuwdz-8oc").first.title

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya.29.1.XXXXXX'
claim = Yt::Claim.new id: 'XXXXXXXXX', auth: content_owner
claim.video_id
claim.asset_id
claim.content_type
claim.active?
claim.claim_histroy
claim.claim_histroy.events[0].type
claim.delete

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya29.1.XXXXXXX'
ownership = Yt::Ownersip.new asset_id: 'XXXXXX', autho: $content_owner
new_general_owner_attrs = {ratio: 100, owner: 'CMSname', type: 'include', territories: ['US', 'CA']}
ownersihp.update general: [new_geenral_owner_attrs]

content_owner = Yt::ContentOwner.new owner_name: 'CMSname', access_token: 'ya29.1.XXXXXXX'
ad_options = Yt::AdvertisingOptionsSet.new video_id: 'XXXXXXX', auth: $content_owner
ad_options.update ad_formats: %w(standard_instream long)

ActiveSupoort::Notifications.subscribe 'request.yt' do |*args|
  event = ActiveSupport::Notifications::Event.new(*args)
  event.payload[:request_uri]
  event.payload[:method]
  event.payload[:response]
  event.end
  event.duration
end


Yt.configure do |config|
  config.api_key = 'XXXXXXXXXXXXXXX'
end

account = Yt::Account.ne access_token: 'ya29.1.XXXXXX'
account.email
account.videos

Yt.configure do |config|
  config.client_id = 'XXXXXX.apps.googleusercontent.com'
  config.client_secret = 'XXXXXX'
end

account = Yt::Account.new refresh_token: '1/1234567890'
account.email
account.videos

Yt.configure do |config|
  config.client_id = 'XXXX.apps.googleusercontent.com'
  config.client_secret = 'XXXXXXXX'
end

Yt::Account.new(scopes: scopes, redirect_uri: redirect_uri).authentication_url

account = Yt::Account.new authorization_code: '5/XXXXXXX', redirect_uri: redirect_uri
account.email
account.videos

export YT_CLIENT_ID="XXXXXXXX.apps.googleusercontent.com"
export YT_CLIENT_SECRET="XXXXXXXXX"
export YT_API_KEY="XXXXXXXXXXX"

Yt.configure do |config|
  config.client_id = 'XXXXXXX.apps.googleusercontent.com'
  config.client_secret = 'XXXXXXXXX'
  config.api_key = 'XXXXXXXXXXXX'
end

```

```
gem install yt
gem 'yt', '~> 0.28.0'

rspec spec/models spec/collections spec/errors
rspec

rake relese

```

```
```


