Ansible *MusicBrainz Search-Server* Role
========================================

https://github.com/metabrainz/search-server


Requirements
------------

 - the ansible role `digris.musicbrainz-mirror` is required

 - to install and build the search index minimum 50GB of disk space is needed

 - Debian 8.x
   + Debian < 8.x: We don't have any reasons to support older versions.
   + ubuntu: Should/could work as well, but has never been tested.


*Note*: Running this playbook takes several hours.


Role Variables
--------------

- `musicbrainz_search_install_directory`: /srv/musicbrainz-search
- `musicbrainz_search_home_directory`: /data/search
- `musicbrainz_search_index_directory`: /data/search/indexdata

Example Playbook
----------------

Minimal usage example:

    - hosts: mb-mirrors
      roles:
        - {
            role: digris.musicbrainz-search,
            index: "/data/search/indexdata",
          }



License
-------

BSD
