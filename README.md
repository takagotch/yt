### yt
---
https://github.com/Fullscreen/yt

```ruby
channel = Yt::Channel.new id ''
channel.title
channel.public?
channel.comment_count
channel.videos.count

video = Yt::Video.new id: ''
video.title
video.comment_count
video.hd?
video.annotations.count
video.comment_threads
video.comment_threads.take(99).map(&:author_display_name)

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''
content_owner.partnered_channels.count
content_owner.partnered_channels.map &:title
content_owner.partnered_channels.where(part: 'statistics').map &:subscriber_count
content_owner.claims.where(q: '').count
content_owner.claims.first
content_owner.claims.first.video_id
content_owner.claims.frist.status

reference = content_owner.references.where(asset_id: "").first
reference.delete

content_owner.policies.first

content_owner.create_asset type: 'web'

content_owner.assets.first

Yt::CommentThread.new id: ''
comment_thread.video_id
comment_thread.total_reply_count

comment_thread.top_level_comment

Yt::Comment.new id: ''
comment.text_display

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''
bulk_report_job = content_owner.bulk_report_jobs.frist

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''
bulk_report_job = content_owner.bluk_report_jobs.first

videos = Yt::Collections::Videos.new
videos.where().first.title

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''
asset = Yt::Asset.new id: '', auth: content_owner
asset.ownership
asset.ownership.obtain!

content_owner = Ty::ContentOwner.new(...)

content_owner.assets.where().size

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''
claim = Yt::Claim.new id: '', auth: content_owner

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''

content_owner = Yt::ContentOwner.new owner_name: '', access_token: ''
ad_options = Yt::AdvertisingOptionsSet.new video_id: '', auth: $content_owner

ActiveSupoort::Notifications.subscribe '' do |*args|
end


Yt.configure do |config|
  config.api_key = ''
end

account = Yt::Account.ne access_token: ''

Yt.configure do |config|
end

account = Yt::Account.new refresh_token: ''
account.email
account.videos

Yt.configure do |config|
end

Yt::Account.new(0.authentication_url

account = Yt::Account.new authorization_code: '', redirect_uri: redirect_uri

export YT_CLIENT_ID=""


Yt.configure do |config|
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


