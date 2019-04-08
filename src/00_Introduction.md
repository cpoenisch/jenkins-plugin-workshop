# Introduction

Welcome to this workshop briefly describing the Jenkins plugin ecosystem and showing how to contribute a change request to an existing plugin.

## Agenda

1. [Jenkins Plugins](10_Plugins.md)
2. [Plugin Development](20_Development.md)
3. [Practice](30_Practice.md)
4. [Resources](40_Resources.md)

## Outline

When working with Jenkins in your daily business there comes a time when you have a special request that can not be solved using Jenkins core features or is not fully implemented in one of the numerous existing plugins. Before writing a new plugin from scratch you are encouraged to contribute to existing plugins.

In this workshop you will learn how to change an existing Jenkins plugin and adapt it to your needs. In particular we will change the [Yet Another Build Visualizer Plugin](https://plugins.jenkins.io/yet-another-build-visualizer) to show the display name of a build instead of the build number.

The practice part will guide you through first setting up your development environment and forking the plugin into your GitHub account. After implementing the requested change and extending the unit tests your contribution is pushed back as a GitHub Pull Request.

Hopefully this workshop will encourage you to actively help improve Jenkins plugins by contributing code, documentation, translations, or tests. **Let's start!**

![Jenkins Superhero](img/superhero.png "Jenkins Superhero")

<sup>(Source: [Jenkins Artwork](https://jenkins.io/artwork/))</sup>
