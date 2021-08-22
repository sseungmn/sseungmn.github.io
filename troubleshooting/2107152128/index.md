---
layout: post
type: troubleshooting
date: 2021-07-15 21:28
category: App
title: Github Page 'cannot load such file -- nokogiri/nokogiri' 에러
subtitle: 깃헙 페이지를 만들 ㄸㅐ 생기는 오ㅠㄹ
writer: 834588
post-header: true
header-img: img/about.jpg
hash-tag: [App, Android, CD, Firebase, Fastlane]
---

## 문제

깃헙 블로그를 하려고 jekyll 테마을 다운 받고 repository에 옮긴 뒤 bundle update를 하니 'cannot load such file -- nokogiri/nokogiri' 에러가 뜬다. 

 

## 해결방법

nokogiri라는 모듈의 버전을 다운그레이드 해주니 해결됐다.

 

Gemfile에 gem 'nokogiri', '~> 1.10.0' 라고 쓰고 저장한 뒤 bundle update를 해주면 잘 설치된다!

그리고 bundle exec jekyll server로 실행해서 http://127.0.0.1:4000에서 확인해보면 잘 뜨는 것을 확인 할 수 있다!
