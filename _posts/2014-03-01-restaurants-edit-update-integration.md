---
layout: post
title:  "Restaurantly#edit, #update  integration tests"
date:   2014-03-01 11:26:42
tags: free ruby coding resources capybara integration testing
language: ruby
categories: editupdateintegration
repo: https://github.com/rubyonrailstutor/restaurantly/tree/restaurant-edit-integration
screencast: "//www.youtube.com/embed/lZiI4nAWh3M?vq=hd1080"
comments: true
---

### INTEGRATION RESTAURANTS#EDIT

> git checkout -b restaurant-edit-integration

> modify spec/features/restaurants_spec.rb

```ruby
  describe "edit links work" do
    context "displays ", :driver => :selenium do
      it "Restaurantly Spots!" do
        visit '/restaurants/new'
        fill_in 'restaurant_name', with: "mc ruby"
        click_button 'submit!'
        visit '/'
        click_link 'edit'
        fill_in 'restaurant_name', with: "mc rails"
        click_button 'update'
        expect(page).to have_content 'mc rails'
      end
    end
  end
```

> rspec spect/features/restaurant_spec.rb

```ruby
  describe "destroy links work" do
    context "displays ", :driver => :selenium do
      it "Restaurantly Spots!" do
        visit '/restaurants/new'
        fill_in 'restaurant_name', with: "mc ruby"
        click_button 'submit!'
        expect(page).to have_content 'mc ruby'
        visit '/'
        click_link 'destroy'
        expect(page).to have_no_content 'mc ruby'
      end
    end
  end
```

> rspec spec/features/restaurant_spec.rb
