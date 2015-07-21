---
layout: post
title: "在brew中切换不同版本的软件"
description: ""
category: ""  
tags: []  
---    
以subversion为例：
    
    brew update
    brew versions subversion
    ## Example: Using Subversion 1.6.17
    #
    # $ brew versions subversion
    # 1.7.3    git checkout f8bf2f3 /usr/local/Library/Formula/subversion.rb
    # 1.7.2    git checkout d89bf83 /usr/local/Library/Formula/subversion.rb
    # 1.6.17   git checkout 6e2d550 /usr/local/Library/Formula/subversion.rb
    # 1.6.16   git checkout 83ed494 /usr/local/Library/Formula/subversion.rb
    # 1.6.15   git checkout 809a18a /usr/local/Library/Formula/subversion.rb
    # 1.6.13   git checkout 7871a99 /usr/local/Library/Formula/subversion.rb
    # 1.6.12   git checkout c99b3ac /usr/local/Library/Formula/subversion.rb
    # 1.6.6    git checkout 8774131 /usr/local/Library/Formula/subversion.rb
    # 1.6.5    git checkout a82e823 /usr/local/Library/Formula/subversion.rb
    # 1.6.3    git checkout 6b6d369 /usr/local/Library/Formula/subversion.rb
    cd `brew --prefix`
    git checkout 6e2d550 /usr/local/Library/Formula/subversion.rb
    brew unlink subversion
    brew install subversion
    brew switch subversion 1.6.17
    git checkout -- Library/Formula/subversion.rb
    
{% include JB/setup %}