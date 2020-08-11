---
  - hosts: prod
    become: yes
    tasks:
    - name: install httpd
      yum:
        name: httpd
        state: present
    - name: start httpd
      service:
        name: httpd
        state: started
    - name: enable httpd
      service:
        name: httpd
        enabled: yes
    - name: copy /Ansible/index.html to /var/www/html
      copy:
        src: /Ansible/index.html
        dest: /var/www/html/
