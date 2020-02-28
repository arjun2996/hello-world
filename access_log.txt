{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 59,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "these are the IP addresses that hit more than 10 times \n",
      "\n",
      "83.149.9.216         >>    23\n",
      "208.115.111.72       >>    22\n",
      "66.249.73.135        >>    11\n",
      "these are the IP addresses that hit more than 5 times \n",
      "\n",
      "83.149.9.216         >>    23\n",
      "208.115.111.72       >>    22\n",
      "66.249.73.135        >>    11\n",
      "218.30.103.62        >>    10\n",
      "134.76.249.10        >>     8\n",
      "93.114.45.13         >>     6\n",
      "110.136.166.128      >>     6\n",
      "46.105.14.53         >>     6\n",
      "91.177.205.119       >>     6\n",
      "81.220.24.207        >>     6\n",
      "86.1.76.62           >>     6\n",
      "105.235.130.196      >>     6\n",
      "54.255.13.204        >>     6\n",
      "68.184.202.186       >>     6\n",
      "97.116.185.190       >>     6\n",
      "90.220.199.149       >>     6\n",
      "36.38.8.174          >>     6\n"
     ]
    }
   ],
   "source": [
    "fie = 'C:/Users/Arjun/Desktop/arjun2996/apache_logs.txt'\n",
    "import collections\n",
    "ipcounter = collections.Counter()\n",
    "fh = open(fie)\n",
    "for logLine in fh:\n",
    "    ip = logLine.split()[0]\n",
    "    ipcounter.update([ip])\n",
    "    \n",
    "def print_fn(x):\n",
    "    \n",
    " print (\"these are the IP addresses that hit more than\", x, \"times\", \"\\n\")\n",
    " for each_tuple in ipcounter.most_common():\n",
    "      ipaddr,count = each_tuple\n",
    "        \n",
    "     #print (ipaddr,count)\n",
    "   \n",
    "      if count > x:\n",
    "      \n",
    "       print ('{:20} >> {:5}'.format(ipaddr,count)  )\n",
    "     \n",
    "      elif count > x:\n",
    "       print ('{:20} >> {:5}'.format(ipaddr,count))\n",
    "print_fn(10)\n",
    "print_fn(5)\n",
    "    \n",
    "\n",
    "    \n",
    "\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "['.android',\n",
       " '.atom',\n",
       " '.aws',\n",
       " '.bash_history',\n",
       " '.conda',\n",
       " '.docker',\n",
       " '.gitconfig',\n",
       " '.ipynb_checkpoints',\n",
       " '.ipython',\n",
       " '.jupyter',\n",
       " '.minikube',\n",
       " '.QtWebEngineProcess',\n",
       " '.ssh',\n",
       " '.viminfo',\n",
       " '.VirtualBox',\n",
       " '.VPN Unlimited',\n",
       " '3D Objects',\n",
       " 'Anaconda3',\n",
       " 'ansel',\n",
       " 'AppData',\n",
       " 'Application Data',\n",
       " 'Contacts',\n",
       " 'Cookies',\n",
       " 'Desktop',\n",
       " 'Documents',\n",
       " 'Downloads',\n",
       " 'Favorites',\n",
       " 'IntelGraphicsProfiles',\n",
       " 'Links',\n",
       " 'Local Settings',\n",
       " 'MicrosoftEdgeBackups',\n",
       " 'Music',\n",
       " 'My Documents',\n",
       " 'NetHood',\n",
       " 'NTUSER.DAT',\n",
       " 'ntuser.dat.LOG1',\n",
       " 'ntuser.dat.LOG2',\n",
       " 'NTUSER.DAT{fd9a35db-49fe-11e9-aa2c-248a07783950}.TM.blf',\n",
       " 'NTUSER.DAT{fd9a35db-49fe-11e9-aa2c-248a07783950}.TMContainer00000000000000000001.regtrans-ms',\n",
       " 'NTUSER.DAT{fd9a35db-49fe-11e9-aa2c-248a07783950}.TMContainer00000000000000000002.regtrans-ms',\n",
       " 'ntuser.ini',\n",
       " 'OneDrive',\n",
       " 'Pictures',\n",
       " 'PrintHood',\n",
       " 'Recent',\n",
       " 'Saved Games',\n",
       " 'Searches',\n",
       " 'SendTo',\n",
       " 'Start Menu',\n",
       " 'Templates',\n",
       " 'terraform-test',\n",
       " 'Untitled.ipynb',\n",
       " 'Untitled1.ipynb',\n",
       " 'Untitled10.ipynb',\n",
       " 'Untitled11.ipynb',\n",
       " 'Untitled12.ipynb',\n",
       " 'Untitled13.ipynb',\n",
       " 'Untitled14.ipynb',\n",
       " 'Untitled15.ipynb',\n",
       " 'Untitled2.ipynb',\n",
       " 'Untitled3.ipynb',\n",
       " 'Untitled4.ipynb',\n",
       " 'Untitled5.ipynb',\n",
       " 'Untitled6.ipynb',\n",
       " 'Untitled7.ipynb',\n",
       " 'Untitled8.ipynb',\n",
       " 'Untitled9.ipynb',\n",
       " 'Videos',\n",
       " 'VirtualBox VMs']"
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "import os\n",
    "os.listdir()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
