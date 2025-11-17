# Gemfile

# 1) 항상 맨 위에 있어야 함
source "https://rubygems.org"

# 2) gemspec 은 source 다음에
gemspec

# 3) 공통 gem 들
gem "csv"
gem "logger"

# Windows 에서만 설치 (권장 방식)
gem "wdm", ">= 0.1.0", platforms: [:mswin, :mingw, :x64_mingw]

# 4) runtime 관련 그룹
group :runtime, :all do

  # dnsruby < 1.72.3 의 warning 회피용 임시 대응
  # Gemfile 안에서 `require 'dnsruby'` 를 호출하면 아직 gem 이 설치 안 된 상태라 에러가 나므로 제거
  gem 'base64', '~> 0.2.0'
end
