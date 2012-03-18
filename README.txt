# Publish Markdown to your Kindle

Like Markdown? Like your Kindle? Want your Markdown documents processed and effortlessly delivered to your Kindle? This is a simple set of scripts for making that happen. They are 'tp' for converting markdown to PDF, 'smtpfile' for sending a file as a MIME attachment, and 'kind', for running the others.

They're pretty easy to use. Extract the scripts in your `$PATH` and set up an alias:

    alias kindle='kind you@example.com you@free.kindle.com smtp.yourserver.com $1'

Your smtp server as specified must be willing to relay mail to free.kindle.com and/or kindle.com.

I haven't tried it @kindle.com (to allow 3G delivery) because I don't care for the charges. I imagine it would work, though.

Once you've done this, you should be able to simply toss your markdown files onto the Kindle.

    eastein@horus:~/docs/txt/chicago$ kindle Chicago\ Neighborhoods\ \&\ Apartments.txt
    Delivered Chicago Neighborhoods & Apartments.pdf.
    eastein@horus:~/docs/txt/chicago$

# Dependencies

You'll want...

* Python 2.6
* dnspython
* markdown
* hml2ps
* ps2pdf
* realpath
